---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CC6AF515-2F43-4E1B-BCBB-8DA23F3C6CBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8687cc00e9ba83c427666e08d0ad46c9aab45e02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054619"
---
# <span data-ttu-id="1a0ba-101">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1a0ba-101">Get-AzureAutomationVariable</span></span>

## <span data-ttu-id="1a0ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a0ba-102">SYNOPSIS</span></span>

<span data-ttu-id="1a0ba-103">Pobiera zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="1a0ba-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="1a0ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a0ba-104">SYNTAX</span></span>

### <span data-ttu-id="1a0ba-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1a0ba-105">ByAll (Default)</span></span>
```
Get-AzureAutomationVariable -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1a0ba-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1a0ba-106">ByName</span></span>
```
Get-AzureAutomationVariable -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a0ba-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1a0ba-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1a0ba-108">Polecenie cmdlet **Get-AzureAutomationVariable** pobiera co najmniej jedno zmienne automatyzacji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1a0ba-108">The **Get-AzureAutomationVariable** cmdlet gets one or more Microsoft Azure Automation variables.</span></span>
<span data-ttu-id="1a0ba-109">Domyślnie zostaną zwrócone wszystkie zmienne.</span><span class="sxs-lookup"><span data-stu-id="1a0ba-109">By default, all variables are returned.</span></span>
<span data-ttu-id="1a0ba-110">Aby uzyskać określoną zmienną, określ jej nazwę.</span><span class="sxs-lookup"><span data-stu-id="1a0ba-110">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="1a0ba-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a0ba-111">EXAMPLES</span></span>

### <span data-ttu-id="1a0ba-112">Przykład 1. Pobieranie zmiennej</span><span class="sxs-lookup"><span data-stu-id="1a0ba-112">Example 1: Get a variable</span></span>
```
PS C:\> $variable = Get-AzureAutomationVariable -AutomationAccountName
PS C:\> "Contoso17" -Name "MyVariable"
PS C:\> $value = $variable.value
```

<span data-ttu-id="1a0ba-113">Te polecenia uzyskują zmienną automatyzacji o nazwie NazwaMojejZmiennej i przypisują jej wartość zmiennej o nazwie $value.</span><span class="sxs-lookup"><span data-stu-id="1a0ba-113">These commands get an Automation variable called MyVariable and assign its value to a variable called $value.</span></span>

## <span data-ttu-id="1a0ba-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a0ba-114">PARAMETERS</span></span>

### <span data-ttu-id="1a0ba-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1a0ba-115">-AutomationAccountName</span></span>
<span data-ttu-id="1a0ba-116">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="1a0ba-116">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="1a0ba-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1a0ba-117">-Name</span></span>
<span data-ttu-id="1a0ba-118">Określa nazwę zmiennej.</span><span class="sxs-lookup"><span data-stu-id="1a0ba-118">Specifies the name of a variable.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0ba-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="1a0ba-119">-Profile</span></span>
<span data-ttu-id="1a0ba-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a0ba-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a0ba-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1a0ba-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a0ba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0ba-122">CommonParameters</span></span>
<span data-ttu-id="1a0ba-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a0ba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0ba-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a0ba-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0ba-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a0ba-125">INPUTS</span></span>

## <span data-ttu-id="1a0ba-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a0ba-126">OUTPUTS</span></span>

### <span data-ttu-id="1a0ba-127">Microsoft. Azure. Commands. Automation. model. zmienna</span><span class="sxs-lookup"><span data-stu-id="1a0ba-127">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="1a0ba-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a0ba-128">NOTES</span></span>

## <span data-ttu-id="1a0ba-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a0ba-129">RELATED LINKS</span></span>

[<span data-ttu-id="1a0ba-130">Nowe — AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1a0ba-130">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="1a0ba-131">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1a0ba-131">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="1a0ba-132">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1a0ba-132">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


