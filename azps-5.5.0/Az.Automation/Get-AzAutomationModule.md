---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: d0ff86b21b96e5aa133f61d0682aa89ed3fea225
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199674"
---
# <span data-ttu-id="36bf4-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="36bf4-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="36bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="36bf4-103">Pobiera metadane dla modułów z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="36bf4-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="36bf4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36bf4-104">SYNTAX</span></span>

### <span data-ttu-id="36bf4-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="36bf4-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36bf4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="36bf4-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36bf4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="36bf4-107">DESCRIPTION</span></span>
<span data-ttu-id="36bf4-108">Polecenie **cmdlet Get-AzAutomationModule** pobiera metadane dla modułów z automatyzacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="36bf4-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="36bf4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36bf4-109">EXAMPLES</span></span>

### <span data-ttu-id="36bf4-110">Przykład 1. Uzyskiwanie wszystkich modułów</span><span class="sxs-lookup"><span data-stu-id="36bf4-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="36bf4-111">To polecenie pobiera wszystkie moduły na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="36bf4-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="36bf4-112">Przykład 2. Uzyskiwanie modułu</span><span class="sxs-lookup"><span data-stu-id="36bf4-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="36bf4-113">To polecenie pobiera moduł o nazwie ContosoModule na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="36bf4-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="36bf4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36bf4-114">PARAMETERS</span></span>

### <span data-ttu-id="36bf4-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="36bf4-115">-AutomationAccountName</span></span>
<span data-ttu-id="36bf4-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera metadane modułu.</span><span class="sxs-lookup"><span data-stu-id="36bf4-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="36bf4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36bf4-117">-DefaultProfile</span></span>
<span data-ttu-id="36bf4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="36bf4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36bf4-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="36bf4-119">-Name</span></span>
<span data-ttu-id="36bf4-120">Określa nazwę modułu, dla którego to polecenie cmdlet pobiera metadane.</span><span class="sxs-lookup"><span data-stu-id="36bf4-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36bf4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36bf4-121">-ResourceGroupName</span></span>
<span data-ttu-id="36bf4-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera metadane modułu.</span><span class="sxs-lookup"><span data-stu-id="36bf4-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="36bf4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36bf4-123">CommonParameters</span></span>
<span data-ttu-id="36bf4-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36bf4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36bf4-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36bf4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36bf4-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36bf4-126">INPUTS</span></span>

### <span data-ttu-id="36bf4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="36bf4-127">System.String</span></span>

## <span data-ttu-id="36bf4-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36bf4-128">OUTPUTS</span></span>

### <span data-ttu-id="36bf4-129">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="36bf4-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="36bf4-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36bf4-130">NOTES</span></span>

## <span data-ttu-id="36bf4-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36bf4-131">RELATED LINKS</span></span>

[<span data-ttu-id="36bf4-132">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="36bf4-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="36bf4-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="36bf4-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="36bf4-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="36bf4-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


