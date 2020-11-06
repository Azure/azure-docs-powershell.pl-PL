---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: c2e03cae02c776b69c424ea3ff685a4118ed94bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548411"
---
# <span data-ttu-id="f093a-101">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f093a-101">New-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="f093a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f093a-102">SYNOPSIS</span></span>
<span data-ttu-id="f093a-103">Tworzy zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f093a-103">Creates an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f093a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f093a-104">SYNTAX</span></span>

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f093a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f093a-105">DESCRIPTION</span></span>
<span data-ttu-id="f093a-106">Polecenie cmdlet **New-AzureRmAutomationVariable** tworzy zmienną w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f093a-106">The **New-AzureRmAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="f093a-107">Aby zaszyfrować zmienną, określ *zaszyfrowany* parametr.</span><span class="sxs-lookup"><span data-stu-id="f093a-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="f093a-108">Nie można zmodyfikować stanu zaszyfrowanego zmiennej po jej utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="f093a-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="f093a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f093a-109">EXAMPLES</span></span>

### <span data-ttu-id="f093a-110">Przykład 1. Tworzenie zmiennej z wartością prostą</span><span class="sxs-lookup"><span data-stu-id="f093a-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f093a-111">To polecenie tworzy zmienną o nazwie StringVariable22 z wartością ciągu na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f093a-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f093a-112">Przykład 2: Tworzenie zmiennej o wartości złożonej</span><span class="sxs-lookup"><span data-stu-id="f093a-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f093a-113">Pierwsze polecenie pobiera maszynę wirtualną przy użyciu Get-AzureVM polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f093a-113">The first command gets a virtual machine by using the Get-AzureVM cmdlet.</span></span>
<span data-ttu-id="f093a-114">Polecenie zapisuje je w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f093a-114">The command stores it in the $VirtualMachine variable.</span></span>

<span data-ttu-id="f093a-115">Drugie polecenie tworzy zmienną o nazwie ComplexVariable01 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f093a-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="f093a-116">To polecenie używa obiektu złożonego w celu uzyskania wartości w tym przypadku maszyny wirtualnej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f093a-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="f093a-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f093a-117">PARAMETERS</span></span>

### <span data-ttu-id="f093a-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f093a-118">-AutomationAccountName</span></span>
<span data-ttu-id="f093a-119">Określa nazwę konta automatyzacji, w którym ma być przechowywana zmienna.</span><span class="sxs-lookup"><span data-stu-id="f093a-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="f093a-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="f093a-120">-Description</span></span>
<span data-ttu-id="f093a-121">Określa opis zmiennej.</span><span class="sxs-lookup"><span data-stu-id="f093a-121">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-122">-Zaszyfrowano</span><span class="sxs-lookup"><span data-stu-id="f093a-122">-Encrypted</span></span>
<span data-ttu-id="f093a-123">Określa, czy to polecenie cmdlet szyfruje wartość zmiennej dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="f093a-123">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f093a-124">-Name</span></span>
<span data-ttu-id="f093a-125">Określa nazwę zmiennej.</span><span class="sxs-lookup"><span data-stu-id="f093a-125">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="f093a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f093a-126">-ResourceGroupName</span></span>
<span data-ttu-id="f093a-127">Określa grupę zasobów, dla której to polecenie cmdlet tworzy zmienną.</span><span class="sxs-lookup"><span data-stu-id="f093a-127">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="f093a-128">-Value</span><span class="sxs-lookup"><span data-stu-id="f093a-128">-Value</span></span>
<span data-ttu-id="f093a-129">Określa wartość zmiennej.</span><span class="sxs-lookup"><span data-stu-id="f093a-129">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f093a-130">-DefaultProfile</span></span>
<span data-ttu-id="f093a-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f093a-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f093a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f093a-132">CommonParameters</span></span>
<span data-ttu-id="f093a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f093a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f093a-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f093a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f093a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f093a-135">INPUTS</span></span>

## <span data-ttu-id="f093a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f093a-136">OUTPUTS</span></span>

### <span data-ttu-id="f093a-137">Microsoft. Azure. Commands. Automation. model. zmienna</span><span class="sxs-lookup"><span data-stu-id="f093a-137">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="f093a-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f093a-138">NOTES</span></span>

## <span data-ttu-id="f093a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f093a-139">RELATED LINKS</span></span>

[<span data-ttu-id="f093a-140">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f093a-140">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="f093a-141">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f093a-141">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="f093a-142">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f093a-142">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


