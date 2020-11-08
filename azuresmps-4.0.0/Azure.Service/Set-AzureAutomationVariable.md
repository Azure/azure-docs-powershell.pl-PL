---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 47664B13-5D63-4012-80E1-7982C8FE22E1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20edd29629cb5dbbfa6f3f538d1530e9c0692e6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055034"
---
# <span data-ttu-id="08bd5-101">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="08bd5-101">Set-AzureAutomationVariable</span></span>

## <span data-ttu-id="08bd5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08bd5-102">SYNOPSIS</span></span>

<span data-ttu-id="08bd5-103">Modyfikuje zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="08bd5-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="08bd5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08bd5-104">SYNTAX</span></span>

### <span data-ttu-id="08bd5-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="08bd5-105">UpdateVariableValue</span></span>
```
Set-AzureAutomationVariable -Name <String> -Encrypted <Boolean> -Value <Object> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="08bd5-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="08bd5-106">UpdateVariableDescription</span></span>
```
Set-AzureAutomationVariable -Name <String> -Description <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="08bd5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="08bd5-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="08bd5-108">Polecenie cmdlet **Set-AzureAutomationVariable** modyfikuje wartość lub opis zmiennej w automatyzacji usługi Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="08bd5-108">The **Set-AzureAutomationVariable** cmdlet modifies the value or description of a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="08bd5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08bd5-109">EXAMPLES</span></span>

### <span data-ttu-id="08bd5-110">Przykład 1. Ustawianie wartości zmiennej</span><span class="sxs-lookup"><span data-stu-id="08bd5-110">Example 1: Set the value of a variable</span></span>
```
PS C:\> Set-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="08bd5-111">To polecenie ustawia nową wartość zmiennej o nazwie MyStringVariable na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="08bd5-111">This command sets a new value for the variable named MyStringVariable in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="08bd5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08bd5-112">PARAMETERS</span></span>

### <span data-ttu-id="08bd5-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="08bd5-113">-AutomationAccountName</span></span>
<span data-ttu-id="08bd5-114">Określa nazwę konta automatyzacji ze zmienną.</span><span class="sxs-lookup"><span data-stu-id="08bd5-114">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="08bd5-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="08bd5-115">-Description</span></span>
<span data-ttu-id="08bd5-116">Określa opis zmiennej.</span><span class="sxs-lookup"><span data-stu-id="08bd5-116">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bd5-117">-Zaszyfrowano</span><span class="sxs-lookup"><span data-stu-id="08bd5-117">-Encrypted</span></span>
<span data-ttu-id="08bd5-118">Wskazuje, czy zmienna ma być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="08bd5-118">Indicates whether to encrypt the variable.</span></span>

```yaml
Type: Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bd5-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="08bd5-119">-Name</span></span>
<span data-ttu-id="08bd5-120">Określa nazwę zmiennej.</span><span class="sxs-lookup"><span data-stu-id="08bd5-120">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="08bd5-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="08bd5-121">-Profile</span></span>
<span data-ttu-id="08bd5-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08bd5-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="08bd5-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="08bd5-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="08bd5-124">-Value</span><span class="sxs-lookup"><span data-stu-id="08bd5-124">-Value</span></span>
<span data-ttu-id="08bd5-125">Określa wartość zmiennej.</span><span class="sxs-lookup"><span data-stu-id="08bd5-125">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bd5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08bd5-126">CommonParameters</span></span>
<span data-ttu-id="08bd5-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08bd5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08bd5-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08bd5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08bd5-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08bd5-129">INPUTS</span></span>

## <span data-ttu-id="08bd5-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08bd5-130">OUTPUTS</span></span>

### <span data-ttu-id="08bd5-131">Microsoft. Azure. Commands. Automation. model. zmienna</span><span class="sxs-lookup"><span data-stu-id="08bd5-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="08bd5-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08bd5-132">NOTES</span></span>

## <span data-ttu-id="08bd5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08bd5-133">RELATED LINKS</span></span>

[<span data-ttu-id="08bd5-134">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="08bd5-134">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="08bd5-135">Nowe — AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="08bd5-135">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="08bd5-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="08bd5-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)


