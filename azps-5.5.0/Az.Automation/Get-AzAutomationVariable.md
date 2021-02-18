---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a8238cf9de2b0b20cb347d16bb74623f6469c03c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201146"
---
# <span data-ttu-id="9d289-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9d289-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="9d289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d289-102">SYNOPSIS</span></span>
<span data-ttu-id="9d289-103">Pobiera zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9d289-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="9d289-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9d289-104">SYNTAX</span></span>

### <span data-ttu-id="9d289-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9d289-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d289-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9d289-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d289-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9d289-107">DESCRIPTION</span></span>
<span data-ttu-id="9d289-108">Polecenie **cmdlet Get-AzAutomationVariable** pobiera jedną lub więcej zmiennych automatyzacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d289-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="9d289-109">Aby uzyskać określoną zmienną, określ jej nazwę.</span><span class="sxs-lookup"><span data-stu-id="9d289-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="9d289-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9d289-110">EXAMPLES</span></span>

### <span data-ttu-id="9d289-111">Przykład 1. Uzyskiwanie zmiennej</span><span class="sxs-lookup"><span data-stu-id="9d289-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="9d289-112">Pierwsze polecenie pobiera zmienną automatyzacji o nazwie Variable06 na koncie o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9d289-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="9d289-113">Polecenie przechowuje ten obiekt w $Variable zmienną.</span><span class="sxs-lookup"><span data-stu-id="9d289-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="9d289-114">Drugie polecenie używa standardowej notacji kropki do właściwości **wartości** $Variable.</span><span class="sxs-lookup"><span data-stu-id="9d289-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="9d289-115">Polecenie przechowuje wartość w $value zmienną.</span><span class="sxs-lookup"><span data-stu-id="9d289-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="9d289-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d289-116">PARAMETERS</span></span>

### <span data-ttu-id="9d289-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9d289-117">-AutomationAccountName</span></span>
<span data-ttu-id="9d289-118">Określa nazwę konta automatyzacji zawierającego zmienne, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d289-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9d289-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d289-119">-DefaultProfile</span></span>
<span data-ttu-id="9d289-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9d289-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d289-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9d289-121">-Name</span></span>
<span data-ttu-id="9d289-122">Określa nazwę zmiennej, która pobiera to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d289-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9d289-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d289-123">-ResourceGroupName</span></span>
<span data-ttu-id="9d289-124">Określa grupę zasobów, dla której to polecenie cmdlet pobiera zmienne.</span><span class="sxs-lookup"><span data-stu-id="9d289-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="9d289-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d289-125">CommonParameters</span></span>
<span data-ttu-id="9d289-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d289-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d289-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d289-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d289-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d289-128">INPUTS</span></span>

### <span data-ttu-id="9d289-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9d289-129">System.String</span></span>

## <span data-ttu-id="9d289-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d289-130">OUTPUTS</span></span>

### <span data-ttu-id="9d289-131">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="9d289-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="9d289-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9d289-132">NOTES</span></span>

## <span data-ttu-id="9d289-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d289-133">RELATED LINKS</span></span>

[<span data-ttu-id="9d289-134">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9d289-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="9d289-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9d289-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="9d289-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9d289-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


