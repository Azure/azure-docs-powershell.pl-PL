---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: 54bbda0226cf2aa374e149bc4b5885b86b31ef12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706806"
---
# <span data-ttu-id="02bfa-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="02bfa-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="02bfa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="02bfa-103">Pobiera metadane modułów z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="02bfa-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="02bfa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02bfa-104">SYNTAX</span></span>

### <span data-ttu-id="02bfa-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="02bfa-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02bfa-106">ByName</span><span class="sxs-lookup"><span data-stu-id="02bfa-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02bfa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="02bfa-107">DESCRIPTION</span></span>
<span data-ttu-id="02bfa-108">Polecenie cmdlet **Get-AzAutomationModule** pobiera metadane modułów z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="02bfa-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="02bfa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02bfa-109">EXAMPLES</span></span>

### <span data-ttu-id="02bfa-110">Przykład 1. Pobierz wszystkie moduły</span><span class="sxs-lookup"><span data-stu-id="02bfa-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="02bfa-111">To polecenie pobiera wszystkie moduły z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="02bfa-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="02bfa-112">Przykład 2: uzyskiwanie modułu</span><span class="sxs-lookup"><span data-stu-id="02bfa-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="02bfa-113">To polecenie Pobiera moduł o nazwie ContosoModule na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="02bfa-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="02bfa-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02bfa-114">PARAMETERS</span></span>

### <span data-ttu-id="02bfa-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="02bfa-115">-AutomationAccountName</span></span>
<span data-ttu-id="02bfa-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera metadane modułu.</span><span class="sxs-lookup"><span data-stu-id="02bfa-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="02bfa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02bfa-117">-DefaultProfile</span></span>
<span data-ttu-id="02bfa-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="02bfa-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02bfa-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02bfa-119">-Name</span></span>
<span data-ttu-id="02bfa-120">Określa nazwę modułu, dla którego to polecenie cmdlet pobiera metadane.</span><span class="sxs-lookup"><span data-stu-id="02bfa-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="02bfa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02bfa-121">-ResourceGroupName</span></span>
<span data-ttu-id="02bfa-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera metadane modułu.</span><span class="sxs-lookup"><span data-stu-id="02bfa-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="02bfa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02bfa-123">CommonParameters</span></span>
<span data-ttu-id="02bfa-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02bfa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02bfa-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02bfa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02bfa-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02bfa-126">INPUTS</span></span>

### <span data-ttu-id="02bfa-127">System. String</span><span class="sxs-lookup"><span data-stu-id="02bfa-127">System.String</span></span>

## <span data-ttu-id="02bfa-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02bfa-128">OUTPUTS</span></span>

### <span data-ttu-id="02bfa-129">Microsoft. Azure. Commands. Automation. model. module</span><span class="sxs-lookup"><span data-stu-id="02bfa-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="02bfa-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02bfa-130">NOTES</span></span>

## <span data-ttu-id="02bfa-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02bfa-131">RELATED LINKS</span></span>

[<span data-ttu-id="02bfa-132">Nowe — AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="02bfa-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="02bfa-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="02bfa-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="02bfa-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="02bfa-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)

