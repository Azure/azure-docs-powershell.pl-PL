---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054916"
---
# <span data-ttu-id="616dc-101">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="616dc-101">Set-AzureSubscription</span></span>

## <span data-ttu-id="616dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="616dc-102">SYNOPSIS</span></span>
<span data-ttu-id="616dc-103">Zmienia subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="616dc-103">Changes an Azure subscription.</span></span>

## <span data-ttu-id="616dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="616dc-104">SYNTAX</span></span>

### <span data-ttu-id="616dc-105">UpdateSubscriptionByIdParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="616dc-105">UpdateSubscriptionByIdParameterSetName (Default)</span></span>
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="616dc-106">UpdateSubscriptionByNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="616dc-106">UpdateSubscriptionByNameParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="616dc-107">AddSubscriptionParameterSetName</span><span class="sxs-lookup"><span data-stu-id="616dc-107">AddSubscriptionParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="616dc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="616dc-108">DESCRIPTION</span></span>
<span data-ttu-id="616dc-109">Polecenie cmdlet **Set-AzureSubscription** ustala i zmienia właściwości obiektu subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="616dc-109">The **Set-AzureSubscription** cmdlet establishes and changes the properties of an Azure subscription object.</span></span>
<span data-ttu-id="616dc-110">Za pomocą tego polecenia cmdlet można pracować w ramach subskrypcji platformy Azure, która nie jest domyślną subskrypcją, ani na zmianę bieżącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="616dc-110">You can use this cmdlet to work in an Azure subscription that is not your default subscription or to change your current storage account.</span></span>
<span data-ttu-id="616dc-111">Aby uzyskać informacje o bieżących i domyślnych subskrypcjach, zobacz polecenie cmdlet **SELECT-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="616dc-111">For information about current and default subscriptions, see the **Select-AzureSubscription** cmdlet.</span></span>

<span data-ttu-id="616dc-112">To polecenie cmdlet działa w ramach obiektu subskrypcji platformy Azure, a nie Twojej bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="616dc-112">This cmdlet operates on an Azure subscription object, not your actual Azure subscription.</span></span>
<span data-ttu-id="616dc-113">Aby utworzyć i zainicjować obsługę administracyjną subskrypcji platformy Azure, odwiedź witrynę [Azure Portal](https://azure.microsoft.com/) ( https://azure.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="616dc-113">To create and provision an Azure subscription, visit the [Azure Portal](https://azure.microsoft.com/) (https://azure.microsoft.com/).</span></span>

<span data-ttu-id="616dc-114">To polecenie cmdlet zmienia dane w pliku danych subskrypcji, które tworzysz po użyciu polecenia cmdlet **Add-AzureAccount** lub **Import-AzurePublishSettingsFile** w celu dodania konta platformy Azure do programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="616dc-114">This cmdlet changes the data in the subscription data file that you create when you use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** cmdlet to add an Azure account to Windows PowerShell.</span></span>

<span data-ttu-id="616dc-115">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="616dc-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="616dc-116">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="616dc-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="616dc-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="616dc-117">EXAMPLES</span></span>

### <span data-ttu-id="616dc-118">Przykład 1. Jeśli zmienisz istniejące subscription1</span><span class="sxs-lookup"><span data-stu-id="616dc-118">Example 1: Change an existing subscription1</span></span>
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

<span data-ttu-id="616dc-119">W tym przykładzie zmienisz certyfikat subskrypcji o nazwie ContosoEngineering.</span><span class="sxs-lookup"><span data-stu-id="616dc-119">This example changes the certificate for the subscription named ContosoEngineering.</span></span>

### <span data-ttu-id="616dc-120">Przykład 2: zmienianie punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="616dc-120">Example 2: Change the service endpoint</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

<span data-ttu-id="616dc-121">To polecenie umożliwia dodanie lub zmianę niestandardowego punktu końcowego usługi dla subskrypcji ContosoEngineering.</span><span class="sxs-lookup"><span data-stu-id="616dc-121">This command adds or changes a custom service endpoint for the ContosoEngineering subscription.</span></span>

### <span data-ttu-id="616dc-122">Przykład 3: czyszczenie wartości właściwości</span><span class="sxs-lookup"><span data-stu-id="616dc-122">Example 3: Clear property values</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

<span data-ttu-id="616dc-123">To polecenie ustawia wartości właściwości certyfikat i ResourceManagerEndpoint na null ($Null).</span><span class="sxs-lookup"><span data-stu-id="616dc-123">This command sets the values of the Certificate and ResourceManagerEndpoint properties to null ($Null).</span></span>
<span data-ttu-id="616dc-124">Spowoduje to wyczyszczenie wartości tych właściwości bez zmieniania innych ustawień.</span><span class="sxs-lookup"><span data-stu-id="616dc-124">This clears the values of those properties without changing other settings.</span></span>

### <span data-ttu-id="616dc-125">Przykład 4: używanie alternatywnego pliku danych subskrypcji</span><span class="sxs-lookup"><span data-stu-id="616dc-125">Example 4: Use an alternate subscription data file</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

<span data-ttu-id="616dc-126">To polecenie powoduje zmianę bieżącego konta magazynu subskrypcji usługi ContosoFinance na ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="616dc-126">This command changes the current storage account of the ContosoFinance subscription to ContosoStorage01.</span></span>
<span data-ttu-id="616dc-127">W poleceniu użyto parametru **SubscriptionDataFile** w celu zmiany danych w pliku danych subskrypcji C:\Azure\SubscriptionData.xml.</span><span class="sxs-lookup"><span data-stu-id="616dc-127">The command uses the **SubscriptionDataFile** parameter to change the data in the C:\Azure\SubscriptionData.xml subscription data file.</span></span>
<span data-ttu-id="616dc-128">Domyślnie funkcja **Set-AzureSubscription** używa domyślnego pliku danych subskrypcji w profilu użytkownika mobilnego.</span><span class="sxs-lookup"><span data-stu-id="616dc-128">By default, **Set-AzureSubscription** uses the default subscription data file in your roaming user profile.</span></span>

## <span data-ttu-id="616dc-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="616dc-129">PARAMETERS</span></span>

### <span data-ttu-id="616dc-130">-Certificate</span><span class="sxs-lookup"><span data-stu-id="616dc-130">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616dc-131">-Context</span><span class="sxs-lookup"><span data-stu-id="616dc-131">-Context</span></span>
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616dc-132">-CurrentStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="616dc-132">-CurrentStorageAccountName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="616dc-133">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="616dc-133">-Environment</span></span>
<span data-ttu-id="616dc-134">Określa środowisko Azure.</span><span class="sxs-lookup"><span data-stu-id="616dc-134">Specifies an Azure environment.</span></span>

<span data-ttu-id="616dc-135">Środowisko platformy Azure niezależne wdrożenie platformy Microsoft Azure, takiej jak AzureCloud dla usługi Azure i AzureChinaCloud dla platformy Azure obsługiwanej przez firmę 21Vianet w Chinach.</span><span class="sxs-lookup"><span data-stu-id="616dc-135">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="616dc-136">Lokalne środowiska platformy Azure można też tworzyć, korzystając z pakietu Azure i poleceń cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="616dc-136">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="616dc-137">Aby uzyskać więcej informacji, zobacz [pakiet Azure](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="616dc-137">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="616dc-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="616dc-138">-PassThru</span></span>
<span data-ttu-id="616dc-139">Zwraca wartość $True, jeśli wykonanie polecenia powiedzie się i $False, jeśli nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="616dc-139">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="616dc-140">Domyślnie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="616dc-140">By default, this cmdlet does not return any output.</span></span>
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

### <span data-ttu-id="616dc-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="616dc-141">-Profile</span></span>
<span data-ttu-id="616dc-142">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="616dc-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="616dc-143">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="616dc-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="616dc-144">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="616dc-144">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="616dc-145">Określa punkt końcowy danych Menedżera zasobów platformy Azure, w tym dane dotyczące grup zasobów skojarzonych z kontem.</span><span class="sxs-lookup"><span data-stu-id="616dc-145">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="616dc-146">Aby uzyskać więcej informacji na temat Menedżera zasobów platformy Azure, zobacz [polecenia cmdlet Menedżera zasobów platformy Azure](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) i [Używanie programu Windows PowerShell z Menedżerem zasobów](https://go.microsoft.com/fwlink/?LinkID=394767)  () https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="616dc-146">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="616dc-147">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="616dc-147">-ServiceEndpoint</span></span>
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

### <span data-ttu-id="616dc-148">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="616dc-148">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616dc-149">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="616dc-149">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616dc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="616dc-150">CommonParameters</span></span>
<span data-ttu-id="616dc-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="616dc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="616dc-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="616dc-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="616dc-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="616dc-153">INPUTS</span></span>

### <span data-ttu-id="616dc-154">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="616dc-154">None</span></span>
<span data-ttu-id="616dc-155">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="616dc-155">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="616dc-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="616dc-156">OUTPUTS</span></span>

### <span data-ttu-id="616dc-157">Brak lub system. Boolean</span><span class="sxs-lookup"><span data-stu-id="616dc-157">None or System.Boolean</span></span>
<span data-ttu-id="616dc-158">Po użyciu parametru *PassThru* to polecenie cmdlet zwraca wartość logiczną.</span><span class="sxs-lookup"><span data-stu-id="616dc-158">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="616dc-159">Domyślnie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="616dc-159">By default, this cmdlet does not return any output.</span></span>

## <span data-ttu-id="616dc-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="616dc-160">NOTES</span></span>

## <span data-ttu-id="616dc-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="616dc-161">RELATED LINKS</span></span>

[<span data-ttu-id="616dc-162">Dodaj-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="616dc-162">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="616dc-163">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="616dc-163">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="616dc-164">Import — AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="616dc-164">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="616dc-165">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="616dc-165">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="616dc-166">Wybierz — AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="616dc-166">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)


