---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 7A45DCAD-88DC-40F0-BBF7-0F531A571CA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b941691366c3af821e3a4cdaa7b07c5e958e16
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054411"
---
# <span data-ttu-id="717dd-101">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="717dd-101">Select-AzureSubscription</span></span>

## <span data-ttu-id="717dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="717dd-102">SYNOPSIS</span></span>
<span data-ttu-id="717dd-103">Zmienia bieżące i domyślne subskrypcje platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="717dd-103">Changes the current and default Azure subscriptions.</span></span>

## <span data-ttu-id="717dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="717dd-104">SYNTAX</span></span>

### <span data-ttu-id="717dd-105">SelectSubscriptionByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="717dd-105">SelectSubscriptionByNameParameterSet (Default)</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="717dd-106">SelectDefaultSubscriptionByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="717dd-106">SelectDefaultSubscriptionByNameParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="717dd-107">SelectSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="717dd-107">SelectSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="717dd-108">SelectDefaultSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="717dd-108">SelectDefaultSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="717dd-109">NoCurrentSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="717dd-109">NoCurrentSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoCurrent] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="717dd-110">NoDefaultSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="717dd-110">NoDefaultSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoDefault] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="717dd-111">Opis</span><span class="sxs-lookup"><span data-stu-id="717dd-111">DESCRIPTION</span></span>
<span data-ttu-id="717dd-112">Polecenie cmdlet **SELECT-AzureSubscription** ustawia i czyści bieżące i domyślne subskrypcje platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="717dd-112">The **Select-AzureSubscription** cmdlet sets and clears the current and default Azure subscriptions.</span></span>

<span data-ttu-id="717dd-113">"Bieżący abonament" to subskrypcja używana domyślnie w bieżącej sesji programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="717dd-113">The "current subscription" is the subscription that is used by default in the current Windows PowerShell session.</span></span>
<span data-ttu-id="717dd-114">"Subskrypcja domyślna" jest domyślnie używana we wszystkich sesjach programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="717dd-114">The "default subscription" is used by default in all Windows PowerShell sessions.</span></span>
<span data-ttu-id="717dd-115">Etykieta "bieżąca subskrypcja" umożliwia określenie innej subskrypcji, która ma być używana domyślnie w bieżącej sesji bez zmieniania "subskrypcji domyślnej" dla wszystkich innych sesji.</span><span class="sxs-lookup"><span data-stu-id="717dd-115">The "current subscription" label lets you specify a different subscription to be used by default for the current session without changing the "default subscription" for all other sessions.</span></span>

<span data-ttu-id="717dd-116">Oznaczenie subskrypcji "domyślny" jest zapisywane w pliku danych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="717dd-116">The "default" subscription designation is saved in your subscription data file.</span></span>
<span data-ttu-id="717dd-117">Oznaczenie "bieżące" specyficzne dla sesji nie jest zapisywane.</span><span class="sxs-lookup"><span data-stu-id="717dd-117">The session-specific "current" designation is not saved.</span></span>

<span data-ttu-id="717dd-118">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="717dd-118">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="717dd-119">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="717dd-119">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="717dd-120">Przykłady</span><span class="sxs-lookup"><span data-stu-id="717dd-120">EXAMPLES</span></span>

### <span data-ttu-id="717dd-121">Przykład 1: Ustawianie bieżącego abonamentu</span><span class="sxs-lookup"><span data-stu-id="717dd-121">Example 1: Set the current subscription</span></span>
```
C:\PS> Select-AzureSubscription -Current -SubscriptionName ContosoEngineering
```

<span data-ttu-id="717dd-122">To polecenie powoduje, że bieżący abonament to "ContosoEngineering".</span><span class="sxs-lookup"><span data-stu-id="717dd-122">This command makes "ContosoEngineering" the current subscription.</span></span>

### <span data-ttu-id="717dd-123">Przykład 2: Ustawianie subskrypcji domyślnej</span><span class="sxs-lookup"><span data-stu-id="717dd-123">Example 2: Set the default subscription</span></span>
```
C:\PS> Select-AzureSubscription -Default -SubscriptionName ContosoFinance -SubscriptionDataFile "C:\subs\MySubscriptions.xml"
```

<span data-ttu-id="717dd-124">To polecenie zmieni domyślny abonament na "ContosoFinance".</span><span class="sxs-lookup"><span data-stu-id="717dd-124">This command changes the default subscription to "ContosoFinance."</span></span> <span data-ttu-id="717dd-125">Zapisuje to ustawienie w pliku danych subskrypcji Subscriptions.xmlej zamiast w domyślnym pliku danych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="717dd-125">It saves the setting in the Subscriptions.xml subscription data file, instead of the default subscription data file.</span></span>

## <span data-ttu-id="717dd-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="717dd-126">PARAMETERS</span></span>

### <span data-ttu-id="717dd-127">— Konto</span><span class="sxs-lookup"><span data-stu-id="717dd-127">-Account</span></span>
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

### <span data-ttu-id="717dd-128">-Bieżące</span><span class="sxs-lookup"><span data-stu-id="717dd-128">-Current</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectSubscriptionByIdParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="717dd-129">-Wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="717dd-129">-Default</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectDefaultSubscriptionByNameParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="717dd-130">-Nocurrent</span><span class="sxs-lookup"><span data-stu-id="717dd-130">-NoCurrent</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoCurrentSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="717dd-131">-Nodefault</span><span class="sxs-lookup"><span data-stu-id="717dd-131">-NoDefault</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoDefaultSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="717dd-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="717dd-132">-PassThru</span></span>
<span data-ttu-id="717dd-133">Zwraca wartość $True, jeśli wykonanie polecenia powiedzie się i $False, jeśli nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="717dd-133">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="717dd-134">Domyślnie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="717dd-134">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="717dd-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="717dd-135">-Profile</span></span>
<span data-ttu-id="717dd-136">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="717dd-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="717dd-137">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="717dd-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="717dd-138">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="717dd-138">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByIdParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="717dd-139">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="717dd-139">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectDefaultSubscriptionByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="717dd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="717dd-140">CommonParameters</span></span>
<span data-ttu-id="717dd-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="717dd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="717dd-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="717dd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="717dd-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="717dd-143">INPUTS</span></span>

### <span data-ttu-id="717dd-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="717dd-144">None</span></span>
<span data-ttu-id="717dd-145">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="717dd-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="717dd-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="717dd-146">OUTPUTS</span></span>

### <span data-ttu-id="717dd-147">Brak lub system. Boolean</span><span class="sxs-lookup"><span data-stu-id="717dd-147">None or System.Boolean</span></span>
<span data-ttu-id="717dd-148">W przypadku użycia parametru *PassThru* to polecenie cmdlet zwraca wartość logiczną.</span><span class="sxs-lookup"><span data-stu-id="717dd-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="717dd-149">Domyślnie nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="717dd-149">By default, it does not generate any output.</span></span>

## <span data-ttu-id="717dd-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="717dd-150">NOTES</span></span>

## <span data-ttu-id="717dd-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="717dd-151">RELATED LINKS</span></span>

[<span data-ttu-id="717dd-152">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="717dd-152">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="717dd-153">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="717dd-153">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="717dd-154">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="717dd-154">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


