---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 82c853f6f18f12c1e7005a859a5df924d3555b79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993000"
---
# <span data-ttu-id="9e7ac-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e7ac-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="9e7ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e7ac-102">SYNOPSIS</span></span>
<span data-ttu-id="9e7ac-103">Pobiera konfiguracje dsc z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9e7ac-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="9e7ac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e7ac-104">SYNTAX</span></span>

### <span data-ttu-id="9e7ac-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9e7ac-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e7ac-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9e7ac-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e7ac-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e7ac-107">DESCRIPTION</span></span>
<span data-ttu-id="9e7ac-108">Polecenie **cmdlet Get-AzAutomationDscConfiguration** pobiera konfiguracje APS Desired State Configuration (DSC) z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9e7ac-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="9e7ac-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e7ac-109">EXAMPLES</span></span>

### <span data-ttu-id="9e7ac-110">Przykład 1. Uzyskiwanie wszystkich konfiguracji dsC</span><span class="sxs-lookup"><span data-stu-id="9e7ac-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="9e7ac-111">To polecenie pobiera metadane dla wszystkich konfiguracji dsc w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9e7ac-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9e7ac-112">Przykład 2. Uzyskiwanie konfiguracji dsC według nazwy</span><span class="sxs-lookup"><span data-stu-id="9e7ac-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="9e7ac-113">To polecenie pobiera metadane dla konfiguracji dsC o nazwie MyConfiguration w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9e7ac-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9e7ac-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e7ac-114">PARAMETERS</span></span>

### <span data-ttu-id="9e7ac-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9e7ac-115">-AutomationAccountName</span></span>
<span data-ttu-id="9e7ac-116">Określa nazwę konta automatyzacji zawierającego konfiguracje dsc, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e7ac-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9e7ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e7ac-117">-DefaultProfile</span></span>
<span data-ttu-id="9e7ac-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9e7ac-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e7ac-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9e7ac-119">-Name</span></span>
<span data-ttu-id="9e7ac-120">Określa nazwę konfiguracji dsc, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e7ac-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9e7ac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e7ac-121">-ResourceGroupName</span></span>
<span data-ttu-id="9e7ac-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera konfiguracje DSC.</span><span class="sxs-lookup"><span data-stu-id="9e7ac-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="9e7ac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e7ac-123">CommonParameters</span></span>
<span data-ttu-id="9e7ac-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e7ac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e7ac-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e7ac-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e7ac-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e7ac-126">INPUTS</span></span>

### <span data-ttu-id="9e7ac-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9e7ac-127">System.String</span></span>

## <span data-ttu-id="9e7ac-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e7ac-128">OUTPUTS</span></span>

### <span data-ttu-id="9e7ac-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e7ac-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="9e7ac-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e7ac-130">NOTES</span></span>

## <span data-ttu-id="9e7ac-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e7ac-131">RELATED LINKS</span></span>

[<span data-ttu-id="9e7ac-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e7ac-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="9e7ac-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e7ac-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


