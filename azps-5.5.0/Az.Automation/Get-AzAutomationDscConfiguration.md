---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 0616cb9f2a379e93a01b450ab8a66da95ca9add1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182187"
---
# <span data-ttu-id="17acb-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="17acb-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="17acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17acb-102">SYNOPSIS</span></span>
<span data-ttu-id="17acb-103">Pobiera konfiguracje dsc z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="17acb-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="17acb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17acb-104">SYNTAX</span></span>

### <span data-ttu-id="17acb-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="17acb-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17acb-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="17acb-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17acb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="17acb-107">DESCRIPTION</span></span>
<span data-ttu-id="17acb-108">Polecenie **cmdlet Get-AzAutomationDscConfiguration** pobiera konfiguracje APS Desired State Configuration (DSC) z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="17acb-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="17acb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17acb-109">EXAMPLES</span></span>

### <span data-ttu-id="17acb-110">Przykład 1. Uzyskiwanie wszystkich konfiguracji dsC</span><span class="sxs-lookup"><span data-stu-id="17acb-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="17acb-111">To polecenie pobiera metadane dla wszystkich konfiguracji DSC na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="17acb-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="17acb-112">Przykład 2. Uzyskiwanie konfiguracji dsc według nazwy</span><span class="sxs-lookup"><span data-stu-id="17acb-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="17acb-113">To polecenie pobiera metadane dla konfiguracji dsc o nazwie MyConfiguration na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="17acb-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="17acb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17acb-114">PARAMETERS</span></span>

### <span data-ttu-id="17acb-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="17acb-115">-AutomationAccountName</span></span>
<span data-ttu-id="17acb-116">Określa nazwę konta automatyzacji zawierającego konfiguracje DSC, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17acb-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="17acb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17acb-117">-DefaultProfile</span></span>
<span data-ttu-id="17acb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="17acb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17acb-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="17acb-119">-Name</span></span>
<span data-ttu-id="17acb-120">Określa nazwę konfiguracji dsc, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17acb-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="17acb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17acb-121">-ResourceGroupName</span></span>
<span data-ttu-id="17acb-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera konfiguracje DSC.</span><span class="sxs-lookup"><span data-stu-id="17acb-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="17acb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17acb-123">CommonParameters</span></span>
<span data-ttu-id="17acb-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17acb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17acb-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17acb-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17acb-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17acb-126">INPUTS</span></span>

### <span data-ttu-id="17acb-127">System.String</span><span class="sxs-lookup"><span data-stu-id="17acb-127">System.String</span></span>

## <span data-ttu-id="17acb-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17acb-128">OUTPUTS</span></span>

### <span data-ttu-id="17acb-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="17acb-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="17acb-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17acb-130">NOTES</span></span>

## <span data-ttu-id="17acb-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17acb-131">RELATED LINKS</span></span>

[<span data-ttu-id="17acb-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="17acb-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="17acb-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="17acb-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


