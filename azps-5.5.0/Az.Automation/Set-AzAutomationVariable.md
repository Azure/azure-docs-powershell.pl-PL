---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182115"
---
# <span data-ttu-id="582d0-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="582d0-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="582d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="582d0-102">SYNOPSIS</span></span>
<span data-ttu-id="582d0-103">Modyfikuje zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="582d0-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="582d0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="582d0-104">SYNTAX</span></span>

### <span data-ttu-id="582d0-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="582d0-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="582d0-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="582d0-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="582d0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="582d0-107">DESCRIPTION</span></span>
<span data-ttu-id="582d0-108">Polecenie cmdlet **Set-AzAutomationVariable** modyfikuje wartość lub opis zmiennej w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="582d0-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="582d0-109">Aby zaszyfrować zmienną, określ *parametr Encrypted.*</span><span class="sxs-lookup"><span data-stu-id="582d0-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="582d0-110">Nie można modyfikować zaszyfrowanego stanu zmiennej po utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="582d0-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="582d0-111">Określenie *zaszyfrowanej* dla istniejącej, nie zaszyfrowanej zmiennej kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="582d0-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="582d0-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="582d0-112">EXAMPLES</span></span>

### <span data-ttu-id="582d0-113">Przykład 1. Ustawianie wartości zmiennej</span><span class="sxs-lookup"><span data-stu-id="582d0-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="582d0-114">To polecenie ustawia nową wartość zmiennej o nazwie StringVariable22 na koncie automatyzacji platformy Azure o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="582d0-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="582d0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="582d0-115">PARAMETERS</span></span>

### <span data-ttu-id="582d0-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="582d0-116">-AutomationAccountName</span></span>
<span data-ttu-id="582d0-117">Określa nazwę konta automatyzacji, w którym jest przechowywana zmienna.</span><span class="sxs-lookup"><span data-stu-id="582d0-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="582d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="582d0-118">-DefaultProfile</span></span>
<span data-ttu-id="582d0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="582d0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="582d0-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="582d0-120">-Description</span></span>
<span data-ttu-id="582d0-121">Określa opis zmiennej.</span><span class="sxs-lookup"><span data-stu-id="582d0-121">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582d0-122">— Encrypted</span><span class="sxs-lookup"><span data-stu-id="582d0-122">-Encrypted</span></span>
<span data-ttu-id="582d0-123">Określa, czy polecenie cmdlet szyfruje wartość zmiennej na miejsce do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="582d0-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582d0-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="582d0-124">-Name</span></span>
<span data-ttu-id="582d0-125">Określa nazwę zmiennej, która ma być zmieniana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="582d0-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582d0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="582d0-126">-ResourceGroupName</span></span>
<span data-ttu-id="582d0-127">Określa grupę zasobów, dla której to polecenie cmdlet modyfikuje zmienną.</span><span class="sxs-lookup"><span data-stu-id="582d0-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="582d0-128">— Wartość</span><span class="sxs-lookup"><span data-stu-id="582d0-128">-Value</span></span>
<span data-ttu-id="582d0-129">Określa wartość zmiennej.</span><span class="sxs-lookup"><span data-stu-id="582d0-129">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="582d0-130">CommonParameters</span></span>
<span data-ttu-id="582d0-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="582d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="582d0-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="582d0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="582d0-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="582d0-133">INPUTS</span></span>

### <span data-ttu-id="582d0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="582d0-134">System.String</span></span>

### <span data-ttu-id="582d0-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="582d0-135">System.Boolean</span></span>

### <span data-ttu-id="582d0-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="582d0-136">System.Object</span></span>

## <span data-ttu-id="582d0-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="582d0-137">OUTPUTS</span></span>

### <span data-ttu-id="582d0-138">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="582d0-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="582d0-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="582d0-139">NOTES</span></span>

## <span data-ttu-id="582d0-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="582d0-140">RELATED LINKS</span></span>

[<span data-ttu-id="582d0-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="582d0-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="582d0-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="582d0-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="582d0-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="582d0-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


