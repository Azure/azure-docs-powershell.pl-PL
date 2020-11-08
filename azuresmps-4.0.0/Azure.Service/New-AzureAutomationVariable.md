---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D88C6B17-5D0E-4E23-9C5C-DB38DED9061C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1518c351a67c84e6dacafd1fa8a394051f3bfeac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054897"
---
# <span data-ttu-id="64317-101">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="64317-101">New-AzureAutomationVariable</span></span>

## <span data-ttu-id="64317-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64317-102">SYNOPSIS</span></span>

<span data-ttu-id="64317-103">Tworzy zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="64317-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="64317-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64317-104">SYNTAX</span></span>

```
New-AzureAutomationVariable -Name <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="64317-105">Opis</span><span class="sxs-lookup"><span data-stu-id="64317-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="64317-106">Polecenie cmdlet **New-AzureAutomationVariable** tworzy zmienną w automatyzacji Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64317-106">The **New-AzureAutomationVariable** cmdlet creates a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="64317-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64317-107">EXAMPLES</span></span>

### <span data-ttu-id="64317-108">Przykład 1. Tworzenie nowej zmiennej z wartością prostą</span><span class="sxs-lookup"><span data-stu-id="64317-108">Example 1: Create a new variable with a simple value</span></span>
```
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Encrypted $False -Value "My String"
```

<span data-ttu-id="64317-109">To polecenie tworzy nową zmienną o nazwie MyStringVariable z wartością ciągu na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="64317-109">This command creates a new variable named MyStringVariable with a string value in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="64317-110">Przykład 2: Tworzenie nowej zmiennej o wartości złożonej</span><span class="sxs-lookup"><span data-stu-id="64317-110">Example 2: Create a new variable with a complex value</span></span>
```
PS C:\> $vm = Get-AzureVM -ServiceName "MyVM" -Name "MyVM"
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyComplexVariable" -Encrypted $False -Value $vm
```

<span data-ttu-id="64317-111">Te polecenia tworzą nową zmienną o nazwie MyComplexVariable na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="64317-111">These commands create a new variable called MyComplexVariable in the Automation account named Contoso17.</span></span>
<span data-ttu-id="64317-112">W tym przypadku jest wykorzystywany obiekt złożony, a w tym przypadku obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="64317-112">A complex object is used for its value, in this case a virtual machine object.</span></span>

## <span data-ttu-id="64317-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64317-113">PARAMETERS</span></span>

### <span data-ttu-id="64317-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="64317-114">-AutomationAccountName</span></span>
<span data-ttu-id="64317-115">Określa nazwę konta automatyzacji, w którym zmienna będzie przechowywana.</span><span class="sxs-lookup"><span data-stu-id="64317-115">Specifies the name of the Automation account the variable will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64317-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="64317-116">-Description</span></span>
<span data-ttu-id="64317-117">Określa opis zmiennej.</span><span class="sxs-lookup"><span data-stu-id="64317-117">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64317-118">-Zaszyfrowano</span><span class="sxs-lookup"><span data-stu-id="64317-118">-Encrypted</span></span>
<span data-ttu-id="64317-119">Wskazuje, czy wartość zmiennej powinna być przechowywana w zaszyfrowanej postaci.</span><span class="sxs-lookup"><span data-stu-id="64317-119">Indicates whether the value of the variable should be stored encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64317-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64317-120">-Name</span></span>
<span data-ttu-id="64317-121">Określa nazwę zmiennej.</span><span class="sxs-lookup"><span data-stu-id="64317-121">Specifies a name for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64317-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="64317-122">-Profile</span></span>
<span data-ttu-id="64317-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64317-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="64317-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="64317-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64317-125">-Value</span><span class="sxs-lookup"><span data-stu-id="64317-125">-Value</span></span>
<span data-ttu-id="64317-126">Określa wartość, która ma być przechowywana w zmiennej.</span><span class="sxs-lookup"><span data-stu-id="64317-126">Specifies a value to store in the variable.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64317-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64317-127">CommonParameters</span></span>
<span data-ttu-id="64317-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64317-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64317-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64317-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64317-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64317-130">INPUTS</span></span>

## <span data-ttu-id="64317-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64317-131">OUTPUTS</span></span>

### <span data-ttu-id="64317-132">Microsoft. Azure. Commands. Automation. model. zmienna</span><span class="sxs-lookup"><span data-stu-id="64317-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="64317-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64317-133">NOTES</span></span>

## <span data-ttu-id="64317-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64317-134">RELATED LINKS</span></span>

[<span data-ttu-id="64317-135">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="64317-135">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="64317-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="64317-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="64317-137">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="64317-137">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


