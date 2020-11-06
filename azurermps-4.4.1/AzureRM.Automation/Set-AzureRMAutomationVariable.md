---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 96e7be91319713ca17f6ad443596316513d2bfbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528325"
---
# <span data-ttu-id="b3a10-101">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b3a10-101">Set-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="b3a10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3a10-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a10-103">Modyfikuje zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="b3a10-103">Modifies an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3a10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3a10-104">SYNTAX</span></span>

### <span data-ttu-id="b3a10-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="b3a10-105">UpdateVariableValue</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3a10-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="b3a10-106">UpdateVariableDescription</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3a10-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b3a10-107">DESCRIPTION</span></span>
<span data-ttu-id="b3a10-108">Polecenie cmdlet **Set-AzureRmAutomationVariable** modyfikuje wartość lub opis zmiennej w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b3a10-108">The **Set-AzureRmAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="b3a10-109">Aby zaszyfrować zmienną, określ *zaszyfrowany* parametr.</span><span class="sxs-lookup"><span data-stu-id="b3a10-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="b3a10-110">Nie można zmodyfikować stanu zaszyfrowanego zmiennej po jej utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="b3a10-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="b3a10-111">Określenie *szyfrowania* dla istniejącej, nieszyfrowanej zmiennej kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="b3a10-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="b3a10-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3a10-112">EXAMPLES</span></span>

### <span data-ttu-id="b3a10-113">Przykład 1. Ustawianie wartości zmiennej</span><span class="sxs-lookup"><span data-stu-id="b3a10-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="b3a10-114">To polecenie ustawia nową wartość zmiennej o nazwie StringVariable22 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b3a10-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="b3a10-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3a10-115">PARAMETERS</span></span>

### <span data-ttu-id="b3a10-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b3a10-116">-AutomationAccountName</span></span>
<span data-ttu-id="b3a10-117">Określa nazwę konta automatyzacji, w którym jest przechowywana zmienna.</span><span class="sxs-lookup"><span data-stu-id="b3a10-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="b3a10-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="b3a10-118">-Description</span></span>
<span data-ttu-id="b3a10-119">Określa opis zmiennej.</span><span class="sxs-lookup"><span data-stu-id="b3a10-119">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="b3a10-120">-Zaszyfrowano</span><span class="sxs-lookup"><span data-stu-id="b3a10-120">-Encrypted</span></span>
<span data-ttu-id="b3a10-121">Określa, czy polecenie cmdlet szyfruje wartość zmiennej dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="b3a10-121">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="b3a10-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3a10-122">-Name</span></span>
<span data-ttu-id="b3a10-123">Określa nazwę zmiennej, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="b3a10-123">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b3a10-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a10-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3a10-125">Określa grupę zasobów, dla której to polecenie cmdlet modyfikuje zmienną.</span><span class="sxs-lookup"><span data-stu-id="b3a10-125">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="b3a10-126">-Value</span><span class="sxs-lookup"><span data-stu-id="b3a10-126">-Value</span></span>
<span data-ttu-id="b3a10-127">Określa wartość zmiennej.</span><span class="sxs-lookup"><span data-stu-id="b3a10-127">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="b3a10-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a10-128">-DefaultProfile</span></span>
<span data-ttu-id="b3a10-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a10-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a10-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a10-130">CommonParameters</span></span>
<span data-ttu-id="b3a10-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a10-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a10-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3a10-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a10-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3a10-133">INPUTS</span></span>

## <span data-ttu-id="b3a10-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3a10-134">OUTPUTS</span></span>

### <span data-ttu-id="b3a10-135">Microsoft. Azure. Commands. Automation. model. zmienna</span><span class="sxs-lookup"><span data-stu-id="b3a10-135">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="b3a10-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3a10-136">NOTES</span></span>

## <span data-ttu-id="b3a10-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3a10-137">RELATED LINKS</span></span>

[<span data-ttu-id="b3a10-138">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b3a10-138">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="b3a10-139">Nowe — AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b3a10-139">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="b3a10-140">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b3a10-140">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)


