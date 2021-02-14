---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
ms.openlocfilehash: 11c6c1073f53ba4a4b93fdae02ae6f6eb22e0f04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201802"
---
# <span data-ttu-id="af708-101">Get-AzRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="af708-101">Get-AzRegulatoryComplianceControl</span></span>

## <span data-ttu-id="af708-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af708-102">SYNOPSIS</span></span>
<span data-ttu-id="af708-103">Otrzymuje kontrolę zgodności z przepisami</span><span class="sxs-lookup"><span data-stu-id="af708-103">Gets regulatory compliance controls</span></span>

## <span data-ttu-id="af708-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="af708-104">SYNTAX</span></span>

### <span data-ttu-id="af708-105">SubscriptionLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="af708-105">SubscriptionLevelResource (Default)</span></span>
```
Get-AzRegulatoryComplianceControl [-Name <String>] -StandardName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af708-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="af708-106">ResourceId</span></span>
```
Get-AzRegulatoryComplianceControl -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af708-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="af708-107">DESCRIPTION</span></span>
<span data-ttu-id="af708-108">Uzyskaj szczegółowe informacje dotyczące kontroli lub listę wszystkich kontrolek w ramach określonego standardu zgodności z przepisami.</span><span class="sxs-lookup"><span data-stu-id="af708-108">Get a spcific control details or list all the controls under specific regulatory compliance standard.</span></span>

## <span data-ttu-id="af708-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="af708-109">EXAMPLES</span></span>

### <span data-ttu-id="af708-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="af708-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.1
Name               : A1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Current processing capacity and usage are maintained, monitored, and evaluated to manage capacity
                     demand and to enable the implementation of additional capacity to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.2
Name               : A1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Environmental protections, software, data backup processes, and recovery infrastructure are
                     designed, developed, implemented, operated, maintained, and monitored to meet availability
                     commitments and requirements.
State              : Passed
PassedAssessments  : 3
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.3
Name               : A1.3
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Recovery plan procedures supporting system recovery are tested to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.1
Name               : C1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information is protected during the system design, development, testing,
                     implementation, and change processes in accordance with confidentiality commitments and
                     requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0
```

<span data-ttu-id="af708-111">Uzyskaj wszystkie mechanizmy kontroli zgodnie z określonymi standardami regulacyjną.</span><span class="sxs-lookup"><span data-stu-id="af708-111">Get all controls under specific regulatory standard.</span></span>

### <span data-ttu-id="af708-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="af708-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP" -Name "C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="af708-113">Uzyskaj szczegółowe informacje o kontrolce zgodnie z identyfikatorem kontrolki.</span><span class="sxs-lookup"><span data-stu-id="af708-113">Get specific control details according to control id.</span></span>

### <span data-ttu-id="af708-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="af708-114">Example 3</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="af708-115">Uzyskaj szczegółowe informacje o kontroli zgodnie z identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="af708-115">Get specific control details according to resource id.</span></span>

## <span data-ttu-id="af708-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af708-116">PARAMETERS</span></span>

### <span data-ttu-id="af708-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af708-117">-DefaultProfile</span></span>
<span data-ttu-id="af708-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="af708-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af708-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="af708-119">-Name</span></span>
<span data-ttu-id="af708-120">Identyfikator kontrolki.</span><span class="sxs-lookup"><span data-stu-id="af708-120">Control Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af708-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af708-121">-ResourceId</span></span>
<span data-ttu-id="af708-122">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="af708-122">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af708-123">-StandardName</span><span class="sxs-lookup"><span data-stu-id="af708-123">-StandardName</span></span>
<span data-ttu-id="af708-124">Nazwa standardowa.</span><span class="sxs-lookup"><span data-stu-id="af708-124">Standard Name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af708-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af708-125">CommonParameters</span></span>
<span data-ttu-id="af708-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af708-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af708-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af708-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af708-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af708-128">INPUTS</span></span>

### <span data-ttu-id="af708-129">System.String</span><span class="sxs-lookup"><span data-stu-id="af708-129">System.String</span></span>

## <span data-ttu-id="af708-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af708-130">OUTPUTS</span></span>

### <span data-ttu-id="af708-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="af708-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span></span>

## <span data-ttu-id="af708-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="af708-132">NOTES</span></span>

## <span data-ttu-id="af708-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af708-133">RELATED LINKS</span></span>
