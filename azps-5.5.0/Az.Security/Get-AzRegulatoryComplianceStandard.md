---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: a554a0adcdf8692f054becb5891cdd0c20203911
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178603"
---
# <span data-ttu-id="99775-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="99775-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="99775-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99775-102">SYNOPSIS</span></span>
<span data-ttu-id="99775-103">Spełnia standardy zgodności z przepisami</span><span class="sxs-lookup"><span data-stu-id="99775-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="99775-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99775-104">SYNTAX</span></span>

### <span data-ttu-id="99775-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="99775-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99775-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="99775-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99775-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="99775-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99775-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="99775-108">DESCRIPTION</span></span>
<span data-ttu-id="99775-109">Uzyskaj szczegółowe informacje dotyczące zgodności z przepisami lub wymień wszystkie standardy zgodności z przepisami w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="99775-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="99775-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99775-110">EXAMPLES</span></span>

### <span data-ttu-id="99775-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99775-111">Example 1</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/Azure-CIS-1.1.0
Name                : Azure-CIS-1.1.0
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 20
FailedControls      : 4
SkippedControls     : 0
UnsupportedControls : 87

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/ISO-27001
Name                : ISO-27001
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 9
FailedControls      : 10
SkippedControls     : 2
UnsupportedControls : 93

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/PCI-DSS-3.2.1
Name                : PCI-DSS-3.2.1
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 13
FailedControls      : 32
SkippedControls     : 0
UnsupportedControls : 187

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="99775-112">Uzyskaj wszystkie standardy zgodności z przepisami w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="99775-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="99775-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="99775-113">Example 2</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -Name "SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="99775-114">Szczegółowe informacje o określonym standardzie zgodności z przepisami należy uzyskać zgodnie ze standardową nazwą.</span><span class="sxs-lookup"><span data-stu-id="99775-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="99775-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="99775-115">Example 3</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplianceStandards/SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="99775-116">Uzyskaj szczegółowe informacje o określonym standardzie zgodności z przepisami zgodnie z identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="99775-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="99775-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99775-117">PARAMETERS</span></span>

### <span data-ttu-id="99775-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99775-118">-DefaultProfile</span></span>
<span data-ttu-id="99775-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="99775-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99775-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="99775-120">-Name</span></span>
<span data-ttu-id="99775-121">Nazwa standardowa.</span><span class="sxs-lookup"><span data-stu-id="99775-121">Standard name.</span></span>

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

### <span data-ttu-id="99775-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99775-122">-ResourceId</span></span>
<span data-ttu-id="99775-123">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="99775-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="99775-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99775-124">CommonParameters</span></span>
<span data-ttu-id="99775-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99775-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99775-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99775-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99775-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99775-127">INPUTS</span></span>

### <span data-ttu-id="99775-128">System.String</span><span class="sxs-lookup"><span data-stu-id="99775-128">System.String</span></span>

## <span data-ttu-id="99775-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99775-129">OUTPUTS</span></span>

### <span data-ttu-id="99775-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="99775-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="99775-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99775-131">NOTES</span></span>

## <span data-ttu-id="99775-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99775-132">RELATED LINKS</span></span>
