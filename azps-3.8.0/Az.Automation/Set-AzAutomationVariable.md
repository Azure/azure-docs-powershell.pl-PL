---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896502"
---
# <span data-ttu-id="2c20a-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2c20a-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="2c20a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c20a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c20a-103">Modyfikuje zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="2c20a-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="2c20a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c20a-104">SYNTAX</span></span>

### <span data-ttu-id="2c20a-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="2c20a-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c20a-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="2c20a-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c20a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2c20a-107">DESCRIPTION</span></span>
<span data-ttu-id="2c20a-108">Polecenie cmdlet **Set-AzAutomationVariable** modyfikuje wartość lub opis zmiennej w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2c20a-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="2c20a-109">Aby zaszyfrować zmienną, określ *zaszyfrowany* parametr.</span><span class="sxs-lookup"><span data-stu-id="2c20a-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="2c20a-110">Nie można zmodyfikować stanu zaszyfrowanego zmiennej po jej utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="2c20a-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="2c20a-111">Określenie *szyfrowania* dla istniejącej, nieszyfrowanej zmiennej kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="2c20a-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="2c20a-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c20a-112">EXAMPLES</span></span>

### <span data-ttu-id="2c20a-113">Przykład 1. Ustawianie wartości zmiennej</span><span class="sxs-lookup"><span data-stu-id="2c20a-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="2c20a-114">To polecenie ustawia nową wartość zmiennej o nazwie StringVariable22 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2c20a-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="2c20a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c20a-115">PARAMETERS</span></span>

### <span data-ttu-id="2c20a-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2c20a-116">-AutomationAccountName</span></span>
<span data-ttu-id="2c20a-117">Określa nazwę konta automatyzacji, w którym jest przechowywana zmienna.</span><span class="sxs-lookup"><span data-stu-id="2c20a-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="2c20a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c20a-118">-DefaultProfile</span></span>
<span data-ttu-id="2c20a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2c20a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c20a-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="2c20a-120">-Description</span></span>
<span data-ttu-id="2c20a-121">Określa opis zmiennej.</span><span class="sxs-lookup"><span data-stu-id="2c20a-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="2c20a-122">-Zaszyfrowano</span><span class="sxs-lookup"><span data-stu-id="2c20a-122">-Encrypted</span></span>
<span data-ttu-id="2c20a-123">Określa, czy polecenie cmdlet szyfruje wartość zmiennej dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="2c20a-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="2c20a-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c20a-124">-Name</span></span>
<span data-ttu-id="2c20a-125">Określa nazwę zmiennej, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="2c20a-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2c20a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c20a-126">-ResourceGroupName</span></span>
<span data-ttu-id="2c20a-127">Określa grupę zasobów, dla której to polecenie cmdlet modyfikuje zmienną.</span><span class="sxs-lookup"><span data-stu-id="2c20a-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="2c20a-128">-Value</span><span class="sxs-lookup"><span data-stu-id="2c20a-128">-Value</span></span>
<span data-ttu-id="2c20a-129">Określa wartość zmiennej.</span><span class="sxs-lookup"><span data-stu-id="2c20a-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="2c20a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c20a-130">CommonParameters</span></span>
<span data-ttu-id="2c20a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c20a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c20a-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c20a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c20a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c20a-133">INPUTS</span></span>

### <span data-ttu-id="2c20a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2c20a-134">System.String</span></span>

### <span data-ttu-id="2c20a-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c20a-135">System.Boolean</span></span>

### <span data-ttu-id="2c20a-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="2c20a-136">System.Object</span></span>

## <span data-ttu-id="2c20a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c20a-137">OUTPUTS</span></span>

### <span data-ttu-id="2c20a-138">Microsoft. Azure. Commands. Automation. model. zmienna</span><span class="sxs-lookup"><span data-stu-id="2c20a-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="2c20a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c20a-139">NOTES</span></span>

## <span data-ttu-id="2c20a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c20a-140">RELATED LINKS</span></span>

[<span data-ttu-id="2c20a-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2c20a-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="2c20a-142">Nowe — AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2c20a-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="2c20a-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2c20a-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


