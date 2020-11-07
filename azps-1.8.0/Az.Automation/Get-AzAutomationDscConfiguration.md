---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: b400efe3224a4fa4b014b9ac93786cd130d4ce6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710600"
---
# <span data-ttu-id="65a1d-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="65a1d-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="65a1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="65a1d-103">Umożliwia pobieranie konfiguracji DSC z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="65a1d-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="65a1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65a1d-104">SYNTAX</span></span>

### <span data-ttu-id="65a1d-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="65a1d-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65a1d-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="65a1d-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65a1d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="65a1d-107">DESCRIPTION</span></span>
<span data-ttu-id="65a1d-108">Polecenie cmdlet **Get-AzAutomationDscConfiguration** pobiera konfiguracje konfiguracji stanu żądanego (DSC) z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="65a1d-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="65a1d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65a1d-109">EXAMPLES</span></span>

### <span data-ttu-id="65a1d-110">Przykład 1: uzyskiwanie wszystkich konfiguracji DSC</span><span class="sxs-lookup"><span data-stu-id="65a1d-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="65a1d-111">To polecenie pobiera metadane wszystkich konfiguracji DSC na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="65a1d-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="65a1d-112">Przykład 2: Uzyskiwanie konfiguracji DSC według nazwy</span><span class="sxs-lookup"><span data-stu-id="65a1d-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="65a1d-113">To polecenie pobiera metadane konfiguracji DSC o nazwie moja konfiguracja na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="65a1d-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="65a1d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65a1d-114">PARAMETERS</span></span>

### <span data-ttu-id="65a1d-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="65a1d-115">-AutomationAccountName</span></span>
<span data-ttu-id="65a1d-116">Określa nazwę konta automatyzacji zawierającego konfiguracje DSC, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a1d-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65a1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a1d-117">-DefaultProfile</span></span>
<span data-ttu-id="65a1d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="65a1d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65a1d-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65a1d-119">-Name</span></span>
<span data-ttu-id="65a1d-120">Określa nazwę konfiguracji DSC, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a1d-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65a1d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65a1d-121">-ResourceGroupName</span></span>
<span data-ttu-id="65a1d-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet ma pobierać konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="65a1d-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65a1d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a1d-123">CommonParameters</span></span>
<span data-ttu-id="65a1d-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a1d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a1d-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65a1d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a1d-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65a1d-126">INPUTS</span></span>

### <span data-ttu-id="65a1d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="65a1d-127">System.String</span></span>

## <span data-ttu-id="65a1d-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65a1d-128">OUTPUTS</span></span>

### <span data-ttu-id="65a1d-129">Microsoft. Azure. Commands. Automation. model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="65a1d-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="65a1d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65a1d-130">NOTES</span></span>

## <span data-ttu-id="65a1d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65a1d-131">RELATED LINKS</span></span>

[<span data-ttu-id="65a1d-132">Eksportowanie — AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="65a1d-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="65a1d-133">Import — AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="65a1d-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


