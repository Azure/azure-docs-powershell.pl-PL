---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: a554a0adcdf8692f054becb5891cdd0c20203911
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222953"
---
# <span data-ttu-id="509bb-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="509bb-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="509bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="509bb-102">SYNOPSIS</span></span>
<span data-ttu-id="509bb-103">Pobiera standardy zgodności regulatoey</span><span class="sxs-lookup"><span data-stu-id="509bb-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="509bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="509bb-104">SYNTAX</span></span>

### <span data-ttu-id="509bb-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="509bb-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="509bb-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="509bb-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="509bb-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="509bb-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="509bb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="509bb-108">DESCRIPTION</span></span>
<span data-ttu-id="509bb-109">Pobierz spcific zgodności z przepisami Satandard szczegóły lub wystaw wszystkie standardy zgodności z przepisami w ramach określonego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="509bb-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="509bb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="509bb-110">EXAMPLES</span></span>

### <span data-ttu-id="509bb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="509bb-111">Example 1</span></span>
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

<span data-ttu-id="509bb-112">Uzyskaj wszystkie standardy zgodności z przepisami w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="509bb-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="509bb-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="509bb-113">Example 2</span></span>
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

<span data-ttu-id="509bb-114">Szczegółowe informacje na temat konkretnego standardu zgodności z przepisami według standardowej nazwy.</span><span class="sxs-lookup"><span data-stu-id="509bb-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="509bb-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="509bb-115">Example 3</span></span>
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

<span data-ttu-id="509bb-116">Szczegółowe informacje na temat konkretnego standardu zgodności z przepisami, zgodnie z identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="509bb-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="509bb-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="509bb-117">PARAMETERS</span></span>

### <span data-ttu-id="509bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="509bb-118">-DefaultProfile</span></span>
<span data-ttu-id="509bb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="509bb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="509bb-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="509bb-120">-Name</span></span>
<span data-ttu-id="509bb-121">Nazwa standardowa.</span><span class="sxs-lookup"><span data-stu-id="509bb-121">Standard name.</span></span>

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

### <span data-ttu-id="509bb-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="509bb-122">-ResourceId</span></span>
<span data-ttu-id="509bb-123">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="509bb-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="509bb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="509bb-124">CommonParameters</span></span>
<span data-ttu-id="509bb-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="509bb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="509bb-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="509bb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="509bb-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="509bb-127">INPUTS</span></span>

### <span data-ttu-id="509bb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="509bb-128">System.String</span></span>

## <span data-ttu-id="509bb-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="509bb-129">OUTPUTS</span></span>

### <span data-ttu-id="509bb-130">Microsoft. Azure. Commands. SecurityCenter. modele. RegulatoryCompliance. PSSecurityRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="509bb-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="509bb-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="509bb-131">NOTES</span></span>

## <span data-ttu-id="509bb-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="509bb-132">RELATED LINKS</span></span>
