# Quick Guide: Apply Page Animations to Remaining Pages

## 🎯 Overview
The PageWrapper and SectionWrapper components are ready to use. Here's how to quickly apply them to the remaining pages.

## 📋 Template Pattern

### 1. **Import Components**
```jsx
import PageWrapper from './PageWrapper'
import SectionWrapper from './SectionWrapper'
```

### 2. **Wrap Page Content**
```jsx
const YourPage = () => {
  return (
    <PageWrapper className="min-h-screen">
      <Navigation />
      
      <div className="max-w-7xl mx-auto px-4 py-8">
        <SectionWrapper index={0}>
          {/* First section */}
        </SectionWrapper>
        
        <SectionWrapper index={1}>
          {/* Second section */}
        </SectionWrapper>
        
        <SectionWrapper index={2}>
          {/* Third section */}
        </SectionWrapper>
      </div>
    </PageWrapper>
  )
}
```

## 🔧 Specific Page Applications

### **SpeechAnalysis.jsx**
```jsx
// Add imports at top
import PageWrapper from './PageWrapper'
import SectionWrapper from './SectionWrapper'

// Wrap sections:
<PageWrapper className="min-h-screen">
  <Navigation />
  <div className="max-w-7xl mx-auto px-4 py-8">
    <SectionWrapper index={0}>
      {/* Header section */}
    </SectionWrapper>
    
    <SectionWrapper index={1}>
      {/* Upload Form section */}
    </SectionWrapper>
    
    {loading && (
      <SectionWrapper index={2}>
        {/* Loading section */}
      </SectionWrapper>
    )}
    
    {analysis && (
      <SectionWrapper index={2}>
        {/* Analysis Results - all sections */}
      </SectionWrapper>
    )}
  </div>
</PageWrapper>
```

### **HistoryPage.jsx**
```jsx
// Add imports at top
import PageWrapper from './PageWrapper'
import SectionWrapper from './SectionWrapper'

// Wrap sections:
<PageWrapper className="min-h-screen">
  <Navigation />
  <div className="max-w-7xl mx-auto px-4 py-8">
    <SectionWrapper index={0}>
      {/* Header */}
    </SectionWrapper>
    
    {sessions.length === 0 ? (
      <SectionWrapper index={1}>
        {/* No Data State */}
      </SectionWrapper>
    ) : (
      <>
        <SectionWrapper index={1}>
          {/* Statistics Overview */}
        </SectionWrapper>
        
        <SectionWrapper index={2}>
          {/* Progress Charts */}
        </SectionWrapper>
        
        <SectionWrapper index={3}>
          {/* Recent Sessions */}
        </SectionWrapper>
      </>
    )}
  </div>
</PageWrapper>
```

### **InterviewMode.jsx**
```jsx
// Add imports at top
import PageWrapper from './PageWrapper'
import SectionWrapper from './SectionWrapper'

// Wrap sections:
<PageWrapper className="min-h-screen">
  <Navigation />
  <div className="max-w-7xl mx-auto px-4 py-8">
    <SectionWrapper index={0}>
      {/* Header */}
    </SectionWrapper>
    
    <SectionWrapper index={1}>
      {/* Question Selection */}
    </SectionWrapper>
    
    <SectionWrapper index={2}>
      {/* Audio Upload */}
    </SectionWrapper>
    
    {loading && (
      <SectionWrapper index={3}>
        {/* Loading */}
      </SectionWrapper>
    )}
    
    {analysis && (
      <SectionWrapper index={3}>
        {/* Analysis Results - all sections */}
      </SectionWrapper>
    )}
  </div>
</PageWrapper>
```

## ⚡ Quick Implementation Steps

1. **Add imports** to each page component
2. **Replace outermost div** with `<PageWrapper className="min-h-screen">`
3. **Wrap major sections** with `<SectionWrapper index={n}>`
4. **Increment index** for each section (0, 1, 2, 3...)
5. **Test in browser** - animations should be visible immediately

## 🎨 Animation Behavior

- **Page loads**: Fade-in with 8px upward motion over 0.6s
- **Sections**: Staggered appearance with 0.1s delay between each
- **Performance**: GPU-accelerated, 60fps smooth animations
- **Professional**: Subtle, non-distracting enhancement

## ✅ Current Status

- ✅ **Dashboard**: Fully implemented with 3 staggered sections
- 🔄 **SpeechAnalysis**: Ready to implement
- 🔄 **HistoryPage**: Ready to implement  
- 🔄 **InterviewMode**: Ready to implement

## 🚀 Test Results

Visit http://localhost:5173 and navigate between pages to see:
- Smooth page entrance animations
- Staggered section appearances
- Professional, subtle motion effects
- Enhanced user experience without distraction