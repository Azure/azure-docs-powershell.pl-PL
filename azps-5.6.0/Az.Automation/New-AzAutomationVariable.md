---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: d5058a3741bfaf598793f81ae030541d26aa4aa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956481"
---
# <span data-ttu-id="8187d-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8187d-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="8187d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8187d-102">SYNOPSIS</span></span>
<span data-ttu-id="8187d-103">Tworzy zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="8187d-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="8187d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8187d-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8187d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8187d-105">DESCRIPTION</span></span>
<span data-ttu-id="8187d-106">Polecenie **cmdlet New-AzAutomationVariable** tworzy zmienną w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8187d-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="8187d-107">Aby zaszyfrować zmienną, określ *parametr Encrypted.*</span><span class="sxs-lookup"><span data-stu-id="8187d-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="8187d-108">Nie można modyfikować zaszyfrowanego stanu zmiennej po utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="8187d-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="8187d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8187d-109">EXAMPLES</span></span>

### <span data-ttu-id="8187d-110">Przykład 1. Tworzenie zmiennej o prostej wartości</span><span class="sxs-lookup"><span data-stu-id="8187d-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8187d-111">To polecenie tworzy zmienną o nazwie StringVariable22 z wartością ciągu w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8187d-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8187d-112">Przykład 2. Tworzenie zmiennej o wartości złożonej</span><span class="sxs-lookup"><span data-stu-id="8187d-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8187d-113">Pierwsze polecenie otrzymuje maszynę wirtualną przy użyciu Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8187d-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="8187d-114">Polecenie przechowuje je w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="8187d-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="8187d-115">Drugie polecenie tworzy zmienną o nazwie ComplexVariable01 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8187d-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="8187d-116">To polecenie używa złożonego obiektu jako wartości, w tym przypadku maszyny wirtualnej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8187d-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="8187d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8187d-117">PARAMETERS</span></span>

### <span data-ttu-id="8187d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8187d-118">-AutomationAccountName</span></span>
<span data-ttu-id="8187d-119">Określa nazwę konta automatyzacji, w którym ma być zapisywana zmienna.</span><span class="sxs-lookup"><span data-stu-id="8187d-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="8187d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8187d-120">-DefaultProfile</span></span>
<span data-ttu-id="8187d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8187d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8187d-122">— Opis</span><span class="sxs-lookup"><span data-stu-id="8187d-122">-Description</span></span>
<span data-ttu-id="8187d-123">Określa opis zmiennej.</span><span class="sxs-lookup"><span data-stu-id="8187d-123">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="8187d-124">— Encrypted</span><span class="sxs-lookup"><span data-stu-id="8187d-124">-Encrypted</span></span>
<span data-ttu-id="8187d-125">Określa, czy to polecenie cmdlet szyfruje wartość zmiennej dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="8187d-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="8187d-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8187d-126">-Name</span></span>
<span data-ttu-id="8187d-127">Określa nazwę zmiennej.</span><span class="sxs-lookup"><span data-stu-id="8187d-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="8187d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8187d-128">-ResourceGroupName</span></span>
<span data-ttu-id="8187d-129">Określa grupę zasobów, dla której to polecenie cmdlet tworzy zmienną.</span><span class="sxs-lookup"><span data-stu-id="8187d-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="8187d-130">— Wartość</span><span class="sxs-lookup"><span data-stu-id="8187d-130">-Value</span></span>
<span data-ttu-id="8187d-131">Określa wartość zmiennej.</span><span class="sxs-lookup"><span data-stu-id="8187d-131">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="8187d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8187d-132">CommonParameters</span></span>
<span data-ttu-id="8187d-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8187d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8187d-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8187d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8187d-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8187d-135">INPUTS</span></span>

### <span data-ttu-id="8187d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8187d-136">System.String</span></span>

### <span data-ttu-id="8187d-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8187d-137">System.Boolean</span></span>

### <span data-ttu-id="8187d-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="8187d-138">System.Object</span></span>

## <span data-ttu-id="8187d-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8187d-139">OUTPUTS</span></span>

### <span data-ttu-id="8187d-140">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="8187d-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="8187d-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8187d-141">NOTES</span></span>

## <span data-ttu-id="8187d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8187d-142">RELATED LINKS</span></span>

[<span data-ttu-id="8187d-143">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8187d-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="8187d-144">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8187d-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="8187d-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8187d-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


