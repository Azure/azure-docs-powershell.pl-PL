---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: bc0fb96ace958761f4d6b12b73ac46b93d9a0143
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710461"
---
# <span data-ttu-id="94eaa-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="94eaa-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="94eaa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="94eaa-103">Modyfikuje zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="94eaa-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="94eaa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94eaa-104">SYNTAX</span></span>

### <span data-ttu-id="94eaa-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="94eaa-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94eaa-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="94eaa-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94eaa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="94eaa-107">DESCRIPTION</span></span>
<span data-ttu-id="94eaa-108">Polecenie cmdlet **Set-AzAutomationVariable** modyfikuje wartość lub opis zmiennej w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="94eaa-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="94eaa-109">Aby zaszyfrować zmienną, określ *zaszyfrowany* parametr.</span><span class="sxs-lookup"><span data-stu-id="94eaa-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="94eaa-110">Nie można zmodyfikować stanu zaszyfrowanego zmiennej po jej utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="94eaa-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="94eaa-111">Określenie *szyfrowania* dla istniejącej, nieszyfrowanej zmiennej kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="94eaa-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="94eaa-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94eaa-112">EXAMPLES</span></span>

### <span data-ttu-id="94eaa-113">Przykład 1. Ustawianie wartości zmiennej</span><span class="sxs-lookup"><span data-stu-id="94eaa-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="94eaa-114">To polecenie ustawia nową wartość zmiennej o nazwie StringVariable22 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="94eaa-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="94eaa-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94eaa-115">PARAMETERS</span></span>

### <span data-ttu-id="94eaa-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="94eaa-116">-AutomationAccountName</span></span>
<span data-ttu-id="94eaa-117">Określa nazwę konta automatyzacji, w którym jest przechowywana zmienna.</span><span class="sxs-lookup"><span data-stu-id="94eaa-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="94eaa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94eaa-118">-DefaultProfile</span></span>
<span data-ttu-id="94eaa-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="94eaa-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94eaa-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="94eaa-120">-Description</span></span>
<span data-ttu-id="94eaa-121">Określa opis zmiennej.</span><span class="sxs-lookup"><span data-stu-id="94eaa-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="94eaa-122">-Zaszyfrowano</span><span class="sxs-lookup"><span data-stu-id="94eaa-122">-Encrypted</span></span>
<span data-ttu-id="94eaa-123">Określa, czy polecenie cmdlet szyfruje wartość zmiennej dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="94eaa-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="94eaa-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="94eaa-124">-Name</span></span>
<span data-ttu-id="94eaa-125">Określa nazwę zmiennej, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="94eaa-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="94eaa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94eaa-126">-ResourceGroupName</span></span>
<span data-ttu-id="94eaa-127">Określa grupę zasobów, dla której to polecenie cmdlet modyfikuje zmienną.</span><span class="sxs-lookup"><span data-stu-id="94eaa-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="94eaa-128">-Value</span><span class="sxs-lookup"><span data-stu-id="94eaa-128">-Value</span></span>
<span data-ttu-id="94eaa-129">Określa wartość zmiennej.</span><span class="sxs-lookup"><span data-stu-id="94eaa-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="94eaa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94eaa-130">CommonParameters</span></span>
<span data-ttu-id="94eaa-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94eaa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94eaa-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94eaa-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94eaa-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94eaa-133">INPUTS</span></span>

### <span data-ttu-id="94eaa-134">System. String</span><span class="sxs-lookup"><span data-stu-id="94eaa-134">System.String</span></span>

### <span data-ttu-id="94eaa-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94eaa-135">System.Boolean</span></span>

### <span data-ttu-id="94eaa-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="94eaa-136">System.Object</span></span>

## <span data-ttu-id="94eaa-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94eaa-137">OUTPUTS</span></span>

### <span data-ttu-id="94eaa-138">Microsoft. Azure. Commands. Automation. model. zmienna</span><span class="sxs-lookup"><span data-stu-id="94eaa-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="94eaa-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94eaa-139">NOTES</span></span>

## <span data-ttu-id="94eaa-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94eaa-140">RELATED LINKS</span></span>

[<span data-ttu-id="94eaa-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="94eaa-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="94eaa-142">Nowe — AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="94eaa-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="94eaa-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="94eaa-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


