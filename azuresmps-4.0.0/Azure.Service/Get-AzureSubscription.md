---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054503"
---
# <span data-ttu-id="013ee-101">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="013ee-101">Get-AzureSubscription</span></span>

## <span data-ttu-id="013ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="013ee-102">SYNOPSIS</span></span>
<span data-ttu-id="013ee-103">Pobiera subskrypcje platformy Azure na koncie platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="013ee-103">Gets  Azure subscriptions in Azure account.</span></span>

## <span data-ttu-id="013ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="013ee-104">SYNTAX</span></span>

### <span data-ttu-id="013ee-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="013ee-105">ByName (Default)</span></span>
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="013ee-106">ById</span><span class="sxs-lookup"><span data-stu-id="013ee-106">ById</span></span>
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="013ee-107">Domyślne</span><span class="sxs-lookup"><span data-stu-id="013ee-107">Default</span></span>
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="013ee-108">Bieżącą</span><span class="sxs-lookup"><span data-stu-id="013ee-108">Current</span></span>
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="013ee-109">Opis</span><span class="sxs-lookup"><span data-stu-id="013ee-109">DESCRIPTION</span></span>
<span data-ttu-id="013ee-110">Polecenie cmdlet **Get-AzureSubscription** pobiera abonamenty na koncie platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="013ee-110">The **Get-AzureSubscription** cmdlet gets the subscriptions in your Azure account.</span></span>
<span data-ttu-id="013ee-111">Za pomocą tego polecenia cmdlet możesz uzyskać informacje o subskrypcji i potoku abonamentu do innych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="013ee-111">You can use this cmdlet to get information about the subscription and to pipe the subscription to other cmdlets.</span></span>

<span data-ttu-id="013ee-112">**Get-AzureSubscription** wymaga dostępu do kont platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="013ee-112">**Get-AzureSubscription** requires access to your Azure accounts.</span></span>
<span data-ttu-id="013ee-113">Przed uruchomieniem polecenia **Get-AzureSubscription** należy uruchomić polecenie cmdlet **Add-AzureAccount** lub polecenia cmdlet, które pobierają i instalują plik ustawień publikowania ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span><span class="sxs-lookup"><span data-stu-id="013ee-113">Before you run **Get-AzureSubscription** , you must run the **Add-AzureAccount** cmdlet or the cmdlets that download and install a publish settings file ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span></span>

<span data-ttu-id="013ee-114">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="013ee-114">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="013ee-115">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="013ee-115">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="013ee-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="013ee-116">EXAMPLES</span></span>

### <span data-ttu-id="013ee-117">Przykład 1: Uzyskaj wszystkie subskrypcje</span><span class="sxs-lookup"><span data-stu-id="013ee-117">Example 1: Get all subscriptions</span></span>
```
C:\PS>Get-AzureSubscription
```

<span data-ttu-id="013ee-118">To polecenie pobiera wszystkie subskrypcje na koncie.</span><span class="sxs-lookup"><span data-stu-id="013ee-118">This command gets all subscriptions in the account.</span></span>

### <span data-ttu-id="013ee-119">Przykład 2: Uzyskaj abonament według imienia i nazwiska</span><span class="sxs-lookup"><span data-stu-id="013ee-119">Example 2: Get a subscription by name</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

<span data-ttu-id="013ee-120">To polecenie pobiera tylko subskrypcję "MyProdSubsciption".</span><span class="sxs-lookup"><span data-stu-id="013ee-120">This command gets only the "MyProdSubsciption" subscription.</span></span>

### <span data-ttu-id="013ee-121">Przykład 3: Uzyskaj abonament domyślny</span><span class="sxs-lookup"><span data-stu-id="013ee-121">Example 3: Get the default subscription</span></span>
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

<span data-ttu-id="013ee-122">To polecenie pobiera tylko nazwę subskrypcji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="013ee-122">This command gets only the name of the default subscription.</span></span>
<span data-ttu-id="013ee-123">Polecenie najpierw pobiera subskrypcję, a następnie używa metody z kropką do uzyskania właściwości **abonamentname** subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="013ee-123">The command first gets the subscription and then uses the dot method to get the **SubscriptionName** property of the subscription.</span></span>

### <span data-ttu-id="013ee-124">Przykład 4: uzyskiwanie wybranych właściwości subskrypcji</span><span class="sxs-lookup"><span data-stu-id="013ee-124">Example 4: Get selected subscription properties</span></span>
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

<span data-ttu-id="013ee-125">To polecenie zwraca listę z nazwą i certyfikatem bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="013ee-125">This command returns a list with the name and certificate of the current subscription.</span></span>
<span data-ttu-id="013ee-126">W celu uzyskania bieżącego abonamentu jest używane polecenie **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="013ee-126">It uses a **Get-AzureSubscription** command to get the current subscription.</span></span>
<span data-ttu-id="013ee-127">Następnie przekazuje abonament na polecenie **list format** , które wyświetla zaznaczone właściwości na liście.</span><span class="sxs-lookup"><span data-stu-id="013ee-127">Then it pipes the subscription to a **Format-List** command that displays the selected properties in a list.</span></span>

### <span data-ttu-id="013ee-128">Przykład 5: używanie alternatywnego pliku danych subskrypcji</span><span class="sxs-lookup"><span data-stu-id="013ee-128">Example 5: Use an alternate subscription data file</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

<span data-ttu-id="013ee-129">To polecenie pobiera abonamenty z pliku danych abonamentu C:\Temp\MySubscriptions.xml.</span><span class="sxs-lookup"><span data-stu-id="013ee-129">This command gets subscriptions from  the C:\Temp\MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="013ee-130">Użyj parametru **SubscriptionDataFile** , jeśli po uruchomieniu polecenia cmdlet **Add-AzureAccount** lub **Import-PublishSettingsFile** zostaną określone alternatywne pliki danych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="013ee-130">Use the **SubscriptionDataFile** parameter if you specified an alternate subscription data file when you ran the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="013ee-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="013ee-131">PARAMETERS</span></span>

### <span data-ttu-id="013ee-132">-Bieżące</span><span class="sxs-lookup"><span data-stu-id="013ee-132">-Current</span></span>
<span data-ttu-id="013ee-133">Pobiera tylko bieżący abonament, czyli abonament oznaczony jako "bieżący".</span><span class="sxs-lookup"><span data-stu-id="013ee-133">Gets only the current subscription, that is, the subscription designated as "current."</span></span> <span data-ttu-id="013ee-134">Domyślnie polecenie **Get-AzureSubscription** pobiera wszystkie subskrypcje na kontach platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="013ee-134">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="013ee-135">Aby wyznaczyć abonament jako bieżący, użyj **bieżącego** parametru polecenia cmdlet **SELECT-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="013ee-135">To designate a subscription as "current," use the **Current** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="013ee-136">-Wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="013ee-136">-Default</span></span>
<span data-ttu-id="013ee-137">Pobiera tylko domyślny abonament, czyli abonament oznaczony jako "domyślny".</span><span class="sxs-lookup"><span data-stu-id="013ee-137">Gets only the default subscription, that is, the subscription designated as "default."</span></span> <span data-ttu-id="013ee-138">Domyślnie polecenie **Get-AzureSubscription** pobiera wszystkie subskrypcje na kontach platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="013ee-138">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="013ee-139">Aby wyznaczyć abonament jako "domyślny", użyj **domyślnego** parametru polecenia cmdlet **SELECT-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="013ee-139">To designate a subscription as "default," use the **Default** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="013ee-140">-ExtendedDetails</span><span class="sxs-lookup"><span data-stu-id="013ee-140">-ExtendedDetails</span></span>
<span data-ttu-id="013ee-141">Zwraca informacje o przydziałach dla subskrypcji oprócz ustawień standardowych.</span><span class="sxs-lookup"><span data-stu-id="013ee-141">Returns quota information for the subscription, in addition to the standard settings.</span></span>

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

### <span data-ttu-id="013ee-142">-Profile</span><span class="sxs-lookup"><span data-stu-id="013ee-142">-Profile</span></span>
<span data-ttu-id="013ee-143">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="013ee-143">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="013ee-144">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="013ee-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="013ee-145">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="013ee-145">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="013ee-146">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="013ee-146">-SubscriptionName</span></span>
<span data-ttu-id="013ee-147">Pobiera tylko określoną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="013ee-147">Gets only the specified subscription.</span></span>
<span data-ttu-id="013ee-148">Wprowadź nazwę subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="013ee-148">Enter the subscription name.</span></span>
<span data-ttu-id="013ee-149">W tej wartości uwzględniana jest wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="013ee-149">The value is case-sensitive.</span></span>
<span data-ttu-id="013ee-150">Symbole wieloznaczne nie są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="013ee-150">Wildcard characters are not supported.</span></span>
<span data-ttu-id="013ee-151">Domyślnie polecenie **Get-AzureSubscription** pobiera wszystkie subskrypcje na kontach platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="013ee-151">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="013ee-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="013ee-152">CommonParameters</span></span>
<span data-ttu-id="013ee-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="013ee-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="013ee-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="013ee-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="013ee-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="013ee-155">INPUTS</span></span>

### <span data-ttu-id="013ee-156">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="013ee-156">None</span></span>
<span data-ttu-id="013ee-157">Możesz popotokować dane wejściowe dla właściwości **abonamentname** według nazwy, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="013ee-157">You can pipe input to the **SubscriptionName** property by name, but not by value.</span></span>

## <span data-ttu-id="013ee-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="013ee-158">OUTPUTS</span></span>

### <span data-ttu-id="013ee-159">Microsoft. platformy windowsazure. Commands. Utilities. Common. WindowsAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="013ee-159">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureSubscription</span></span>

## <span data-ttu-id="013ee-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="013ee-160">NOTES</span></span>
* <span data-ttu-id="013ee-161">Get-AzureSubscription pobiera dane z pliku danych subskrypcji, które zostaną utworzone przez polecenia cmdlet **Add-AzureAccount** i **Import-PublishSettingsFile** .</span><span class="sxs-lookup"><span data-stu-id="013ee-161">Get-AzureSubscription gets data from the subscription data file that the **Add-AzureAccount** and **Import-PublishSettingsFile** cmdlets create.</span></span>

## <span data-ttu-id="013ee-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="013ee-162">RELATED LINKS</span></span>

[<span data-ttu-id="013ee-163">Dodaj-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="013ee-163">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="013ee-164">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="013ee-164">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="013ee-165">Import — AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="013ee-165">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="013ee-166">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="013ee-166">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="013ee-167">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="013ee-167">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


