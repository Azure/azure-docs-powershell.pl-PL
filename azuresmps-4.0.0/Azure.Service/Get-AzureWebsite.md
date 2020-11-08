---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055240"
---
# <span data-ttu-id="b6747-101">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b6747-101">Get-AzureWebsite</span></span>

## <span data-ttu-id="b6747-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6747-102">SYNOPSIS</span></span>
<span data-ttu-id="b6747-103">Pobiera witryny sieci Web platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b6747-103">Gets Azure websites in the current subscription.</span></span>

## <span data-ttu-id="b6747-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6747-104">SYNTAX</span></span>

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b6747-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6747-105">DESCRIPTION</span></span>
<span data-ttu-id="b6747-106">Polecenie cmdlet **Get-AzureWebsite** pobiera informacje o witrynach sieci Web platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b6747-106">The **Get-AzureWebsite** cmdlet gets information about Azure websites in the current subscription.</span></span>

<span data-ttu-id="b6747-107">Domyślnie funkcja **Get-AzureWebsite** pobiera wszystkie witryny sieci Web platformy Azure w bieżącej subskrypcji i zwraca obiekt, który dostarcza podstawowych informacji o witrynach.</span><span class="sxs-lookup"><span data-stu-id="b6747-107">By default, **Get-AzureWebsite** gets all Azure websites in the current subscription and returns an object that provides basic information about the sites.</span></span>
<span data-ttu-id="b6747-108">Gdy jest używany parametr *name* , funkcja **Get-AzureWebsite** zwraca obiekt z obszernymi informacjami, w tym szczegóły konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="b6747-108">When you use the *Name* parameter, **Get-AzureWebsite** returns an object with extensive information, including configuration details.</span></span>

<span data-ttu-id="b6747-109">Bieżący abonament to subskrypcja określona jako "Bieżąca".</span><span class="sxs-lookup"><span data-stu-id="b6747-109">The current subscription is the subscription that is designated as "current."</span></span> <span data-ttu-id="b6747-110">Aby znaleźć bieżącą subskrypcję, użyj *bieżącego* parametru polecenia cmdlet [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) .</span><span class="sxs-lookup"><span data-stu-id="b6747-110">To find the current subscription, use the *Current* parameter of the [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) cmdlet.</span></span>
<span data-ttu-id="b6747-111">Aby zmienić bieżącą subskrypcję, użyj polecenia cmdlet [SELECT-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) .</span><span class="sxs-lookup"><span data-stu-id="b6747-111">To change the current subscription, use the [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) cmdlet.</span></span>

<span data-ttu-id="b6747-112">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b6747-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b6747-113">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b6747-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="b6747-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6747-114">EXAMPLES</span></span>

### <span data-ttu-id="b6747-115">Przykład 1: uzyskiwanie wszystkich witryn internetowych w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b6747-115">Example 1: Get all websites in the subscription</span></span>
```
PS C:\> Get-AzureWebsite
```

<span data-ttu-id="b6747-116">To polecenie umożliwia pobieranie wszystkich witryn sieci Web platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b6747-116">This command gets all Azure websites in the current subscription.</span></span>

### <span data-ttu-id="b6747-117">Przykład 2: Uzyskaj witrynę internetową według nazwy</span><span class="sxs-lookup"><span data-stu-id="b6747-117">Example 2: Get a website by name</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

<span data-ttu-id="b6747-118">To polecenie zawiera szczegółowe informacje na temat witryny sieci Web usługi ContosoWeb Azure, w tym informacje o konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="b6747-118">This command gets detailed information about the ContosoWeb Azure website, including configuration information.</span></span>
<span data-ttu-id="b6747-119">Gdy jest używany parametr *name* , funkcja **Get-AzureWebsite** zwraca obiekt **SiteWithConfig** z rozszerzonymi informacjami na temat witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b6747-119">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object with extended information about the website.</span></span>

### <span data-ttu-id="b6747-120">Przykład 3: uzyskiwanie szczegółowych informacji o wszystkich witrynach internetowych</span><span class="sxs-lookup"><span data-stu-id="b6747-120">Example 3: Get detailed information about all websites</span></span>
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

<span data-ttu-id="b6747-121">To polecenie umożliwia pobieranie szczegółowych informacji o wszystkich witrynach internetowych w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b6747-121">This command gets detailed information about all websites in the subscription.</span></span>
<span data-ttu-id="b6747-122">Korzysta z polecenia **Get-AzureWebsite** w celu uzyskania wszystkich witryn internetowych, a następnie użyto polecenia cmdlet **-Object** cmdlet w celu uzyskania każdej witryny sieci Web według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b6747-122">It uses a **Get-AzureWebsite** command to get all websites and then uses the **ForEach-Object** cmdlet to get each website by name.</span></span>

### <span data-ttu-id="b6747-123">Przykład 4: uzyskiwanie informacji o miejscu wdrożenia</span><span class="sxs-lookup"><span data-stu-id="b6747-123">Example 4: Get information about a deployment slot</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

<span data-ttu-id="b6747-124">To polecenie umożliwia wyświetlenie miejsca do wdrożenia przemieszczania w witrynie internetowej ContosoWeb.</span><span class="sxs-lookup"><span data-stu-id="b6747-124">This command gets the Staging deployment slot of the ContosoWeb website.</span></span>
<span data-ttu-id="b6747-125">Miejsca wdrażania umożliwiają testowanie różnych wersji witryny usługi Azure w sieci Web bez konieczności ich publicznego udostępnienia.</span><span class="sxs-lookup"><span data-stu-id="b6747-125">Deployment slots let you test different versions of your Azure website without releasing them to the public.</span></span>

### <span data-ttu-id="b6747-126">Przykład 5: uzyskiwanie wystąpień witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="b6747-126">Example 5: Get website instances</span></span>
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

<span data-ttu-id="b6747-127">W poleceniach w tym przykładzie użyto właściwości Instances witryny sieci Web platformy Azure, aby uzyskać informacje o obecnie uruchomionych wystąpieniach witryn.</span><span class="sxs-lookup"><span data-stu-id="b6747-127">The commands in this example use the Instances property of an Azure website to get information about currently running website instances.</span></span>
<span data-ttu-id="b6747-128">Właściwość **Instances** została dodana do obiektu **SiteWithConfig** w wersji 0.8.3 modułu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6747-128">The **Instances** property was added to the **SiteWithConfig** object in version 0.8.3 of the Azure module.</span></span>

<span data-ttu-id="b6747-129">Pierwsze polecenie pobiera identyfikatory wystąpienia wszystkich obecnie uruchomionych wystąpień witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b6747-129">The first command gets the instance IDs of all currently running instances of a website.</span></span>
<span data-ttu-id="b6747-130">Drugie polecenie pobiera liczbę uruchomionych wystąpień witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b6747-130">The second command gets the number of running instances of the website.</span></span>
<span data-ttu-id="b6747-131">Właściwości **Count** można użyć w dowolnej tablicy.</span><span class="sxs-lookup"><span data-stu-id="b6747-131">You can use the **Count** property on any array.</span></span>

## <span data-ttu-id="b6747-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6747-132">PARAMETERS</span></span>

### <span data-ttu-id="b6747-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6747-133">-Name</span></span>
<span data-ttu-id="b6747-134">Pobiera szczegółowe informacje o konfiguracji dotyczące określonej witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b6747-134">Gets detailed configuration information about the specified website.</span></span>
<span data-ttu-id="b6747-135">Wprowadź nazwę jednej witryny sieci Web w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b6747-135">Enter the name of one website in the subscription.</span></span>
<span data-ttu-id="b6747-136">Domyślnie polecenie **Get-AzureWebsite** pobiera wszystkie witryny sieci Web w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b6747-136">By default, **Get-AzureWebsite** gets all websites in the current subscription.</span></span>
<span data-ttu-id="b6747-137">Wartość *nazwy* nie obsługuje symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="b6747-137">The *Name* value does not support wildcard characters.</span></span>

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

### <span data-ttu-id="b6747-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="b6747-138">-Profile</span></span>
<span data-ttu-id="b6747-139">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6747-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6747-140">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b6747-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6747-141">-Slot</span><span class="sxs-lookup"><span data-stu-id="b6747-141">-Slot</span></span>
<span data-ttu-id="b6747-142">Pobiera określone miejsce wdrożenia witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b6747-142">Gets the specified deployment slot of the website.</span></span>
<span data-ttu-id="b6747-143">Wprowadź nazwę miejsca, na przykład "przemieszczanie" lub "produkcja".</span><span class="sxs-lookup"><span data-stu-id="b6747-143">Enter the slot name, such as "Staging" or "Production".</span></span>
<span data-ttu-id="b6747-144">Aby uzyskać więcej informacji na temat miejsc wdrożenia, zobacz Wdrażanie etapowe w witrynach usługi Microsoft Azure w sieci Web https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .</span><span class="sxs-lookup"><span data-stu-id="b6747-144">For more information about deployment slots, see Staged Deployment on Microsoft Azure Web Siteshttps://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/.</span></span>
<span data-ttu-id="b6747-145">Aby dodać miejsce wdrożenia do istniejącej witryny internetowej platformy Azure, użyj polecenia cmdlet Set-AzureWebsite.</span><span class="sxs-lookup"><span data-stu-id="b6747-145">To add a deployment slot to an existing Azure website, use the Set-AzureWebsite cmdlet.</span></span>

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

### <span data-ttu-id="b6747-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6747-146">CommonParameters</span></span>
<span data-ttu-id="b6747-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6747-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6747-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6747-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6747-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6747-149">INPUTS</span></span>

### <span data-ttu-id="b6747-150">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b6747-150">None</span></span>
<span data-ttu-id="b6747-151">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="b6747-151">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="b6747-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6747-152">OUTPUTS</span></span>

### <span data-ttu-id="b6747-153">Microsoft. platformy windowsazure. Commands. Utilities. Web. Services. webentities. witryna</span><span class="sxs-lookup"><span data-stu-id="b6747-153">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.Site</span></span>
<span data-ttu-id="b6747-154">Domyślnie funkcja **Get-AzureWebsite** zwraca tablicę obiektów **witryny** .</span><span class="sxs-lookup"><span data-stu-id="b6747-154">By default, **Get-AzureWebsite** returns an array of **Site** objects.</span></span>

### <span data-ttu-id="b6747-155">Microsoft. platformy windowsazure. Commands. Utilities. Web. Services. webentities. SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="b6747-155">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.SiteWithConfig</span></span>
<span data-ttu-id="b6747-156">Gdy jest używany parametr *name* , funkcja **Get-AzureWebsite** zwraca obiekt **SiteWithConfig** .</span><span class="sxs-lookup"><span data-stu-id="b6747-156">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object.</span></span>

## <span data-ttu-id="b6747-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6747-157">NOTES</span></span>

## <span data-ttu-id="b6747-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6747-158">RELATED LINKS</span></span>

[<span data-ttu-id="b6747-159">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b6747-159">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="b6747-160">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b6747-160">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="b6747-161">Start — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b6747-161">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="b6747-162">Zatrzymaj — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b6747-162">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="b6747-163">Pokaż — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b6747-163">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


