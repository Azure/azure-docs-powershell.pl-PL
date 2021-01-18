---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: d0ff86b21b96e5aa133f61d0682aa89ed3fea225
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502361"
---
# <span data-ttu-id="19c5a-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="19c5a-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="19c5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="19c5a-103">Pobiera metadane modułów z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="19c5a-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="19c5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19c5a-104">SYNTAX</span></span>

### <span data-ttu-id="19c5a-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="19c5a-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19c5a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="19c5a-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19c5a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="19c5a-107">DESCRIPTION</span></span>
<span data-ttu-id="19c5a-108">Polecenie cmdlet **Get-AzAutomationModule** pobiera metadane modułów z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="19c5a-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="19c5a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19c5a-109">EXAMPLES</span></span>

### <span data-ttu-id="19c5a-110">Przykład 1. Pobierz wszystkie moduły</span><span class="sxs-lookup"><span data-stu-id="19c5a-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="19c5a-111">To polecenie pobiera wszystkie moduły z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="19c5a-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="19c5a-112">Przykład 2: uzyskiwanie modułu</span><span class="sxs-lookup"><span data-stu-id="19c5a-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="19c5a-113">To polecenie Pobiera moduł o nazwie ContosoModule na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="19c5a-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="19c5a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19c5a-114">PARAMETERS</span></span>

### <span data-ttu-id="19c5a-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="19c5a-115">-AutomationAccountName</span></span>
<span data-ttu-id="19c5a-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera metadane modułu.</span><span class="sxs-lookup"><span data-stu-id="19c5a-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="19c5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c5a-117">-DefaultProfile</span></span>
<span data-ttu-id="19c5a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="19c5a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19c5a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="19c5a-119">-Name</span></span>
<span data-ttu-id="19c5a-120">Określa nazwę modułu, dla którego to polecenie cmdlet pobiera metadane.</span><span class="sxs-lookup"><span data-stu-id="19c5a-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="19c5a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c5a-121">-ResourceGroupName</span></span>
<span data-ttu-id="19c5a-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera metadane modułu.</span><span class="sxs-lookup"><span data-stu-id="19c5a-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="19c5a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c5a-123">CommonParameters</span></span>
<span data-ttu-id="19c5a-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c5a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c5a-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c5a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c5a-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19c5a-126">INPUTS</span></span>

### <span data-ttu-id="19c5a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="19c5a-127">System.String</span></span>

## <span data-ttu-id="19c5a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19c5a-128">OUTPUTS</span></span>

### <span data-ttu-id="19c5a-129">Microsoft. Azure. Commands. Automation. model. module</span><span class="sxs-lookup"><span data-stu-id="19c5a-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="19c5a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19c5a-130">NOTES</span></span>

## <span data-ttu-id="19c5a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19c5a-131">RELATED LINKS</span></span>

[<span data-ttu-id="19c5a-132">Nowe — AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="19c5a-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="19c5a-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="19c5a-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="19c5a-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="19c5a-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


