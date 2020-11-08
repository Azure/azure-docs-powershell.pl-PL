---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054599"
---
# <span data-ttu-id="754b4-101">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="754b4-101">Get-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="754b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="754b4-102">SYNOPSIS</span></span>
<span data-ttu-id="754b4-103">Pobiera plik ustawień publikowania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="754b4-103">Downloads the publish settings file for an Azure subscription.</span></span>

## <span data-ttu-id="754b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="754b4-104">SYNTAX</span></span>

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="754b4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="754b4-105">DESCRIPTION</span></span>
<span data-ttu-id="754b4-106">Polecenie cmdlet **Get-AzurePublishSettingsFile** pobiera plik ustawień publikowania dla abonamentu na koncie.</span><span class="sxs-lookup"><span data-stu-id="754b4-106">The **Get-AzurePublishSettingsFile** cmdlet downloads a publish settings file for a subscription in your account.</span></span>
<span data-ttu-id="754b4-107">Po ukończeniu polecenia możesz użyć polecenia cmdlet **Import-PublishSettingsFile** , aby ustawić ustawienia dostępne dla programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="754b4-107">When the command completes, you can use the **Import-PublishSettingsFile** cmdlet to make the settings in the file available to Windows PowerShell.</span></span>

<span data-ttu-id="754b4-108">Aby konto platformy Azure było dostępne dla programu Windows PowerShell, możesz użyć pliku ustawień publikowania lub polecenia cmdlet **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="754b4-108">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="754b4-109">Publikowanie plików ustawień umożliwia przygotowywanie sesji z wyprzedzeniem, aby można było uruchamiać skrypty i zadania w tle bez opieki.</span><span class="sxs-lookup"><span data-stu-id="754b4-109">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="754b4-110">Jednak nie wszystkie usługi obsługują pliki ustawień publikowania.</span><span class="sxs-lookup"><span data-stu-id="754b4-110">However, not all services support publish settings files.</span></span>
<span data-ttu-id="754b4-111">Na przykład moduł **AzureResourceManager** nie obsługuje plików ustawień publikowania.</span><span class="sxs-lookup"><span data-stu-id="754b4-111">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="754b4-112">Po uruchomieniu polecenia **Get-AzurePublishSettingsFile** zostanie otwarta przeglądarka domyślna i zostanie wyświetlony monit o zalogowanie się do konta platformy Azure, wybranie subskrypcji i wybranie lokalizacji systemu plików dla pliku ustawień publikowania.</span><span class="sxs-lookup"><span data-stu-id="754b4-112">When you run **Get-AzurePublishSettingsFile** , it opens your default browser and prompts you to sign into your Azure account, select a subscription, and select a file system location for the publish settings file.</span></span>
<span data-ttu-id="754b4-113">Następnie pobiera plik ustawień publikowania dla subskrypcji do wybranego pliku.</span><span class="sxs-lookup"><span data-stu-id="754b4-113">Then, it downloads the publish settings file for your subscription into the file that you selected.</span></span>

<span data-ttu-id="754b4-114">"Plik ustawień publikowania" to plik XML z rozszerzeniem nazwy pliku publishsettings.</span><span class="sxs-lookup"><span data-stu-id="754b4-114">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span>
<span data-ttu-id="754b4-115">Plik zawiera zakodowany certyfikat, który zawiera poświadczenia zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="754b4-115">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span>

<span data-ttu-id="754b4-116">**Uwaga dotycząca zabezpieczeń:** Pliki ustawień publikowania zawierają poświadczenia, które służą do administrowania subskrypcjami i usługami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="754b4-116">**Security Note:** Publish settings files contains credentials that are used to administer your Azure subscriptions and services.</span></span>
<span data-ttu-id="754b4-117">Jeśli Złośliwi użytkownicy uzyskują dostęp do pliku ustawień publikowania, mogą edytować, tworzyć i usuwać usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="754b4-117">If  malicious users access your publish settings file,  they can edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="754b4-118">Zgodnie z najważniejszymi wskazówkami dotyczącymi zabezpieczeń Zapisz plik w lokalizacji w folderze pobrane pliki lub dokumenty, a następnie usuń go po użyciu polecenia cmdlet **importu-AzurePublishSettingsFile** w celu zaimportowania ustawień.</span><span class="sxs-lookup"><span data-stu-id="754b4-118">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

<span data-ttu-id="754b4-119">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="754b4-119">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="754b4-120">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="754b4-120">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="754b4-121">Przykłady</span><span class="sxs-lookup"><span data-stu-id="754b4-121">EXAMPLES</span></span>

### <span data-ttu-id="754b4-122">Przykład 1: Pobieranie pliku ustawień publikowania</span><span class="sxs-lookup"><span data-stu-id="754b4-122">Example 1: Download a publish settings file</span></span>
```
PS C:\> Get-AzurePublishSettingsFile
```

<span data-ttu-id="754b4-123">To polecenie otwiera przeglądarkę domyślną, nawiązuje połączenie z kontem Windows Azure, a następnie pobiera plik publishsettings dla swojego konta.</span><span class="sxs-lookup"><span data-stu-id="754b4-123">This command opens your default browser, connects to your Windows Azure account, and then downloads the .publishsettings file for your account.</span></span>

### <span data-ttu-id="754b4-124">Przykład 2: Określanie obszaru</span><span class="sxs-lookup"><span data-stu-id="754b4-124">Example 2: Specify a realm</span></span>
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

<span data-ttu-id="754b4-125">To polecenie pobiera plik ustawień publikowania dla konta w domenie contoso.com.</span><span class="sxs-lookup"><span data-stu-id="754b4-125">This command downloads the publish settings file for an account in the contoso.com domain.</span></span>
<span data-ttu-id="754b4-126">Użyj polecenia z parametrem **Realm** , gdy logujesz się do platformy Azure przy użyciu konta organizacji, a nie konta Microsoft.</span><span class="sxs-lookup"><span data-stu-id="754b4-126">Use a command with the **Realm** parameter when you sign into Azure with an organizational account, instead of a Microsoft account.</span></span>

## <span data-ttu-id="754b4-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="754b4-127">PARAMETERS</span></span>

### <span data-ttu-id="754b4-128">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="754b4-128">-Environment</span></span>
<span data-ttu-id="754b4-129">Określa środowisko Azure.</span><span class="sxs-lookup"><span data-stu-id="754b4-129">Specifies an Azure environment.</span></span>

<span data-ttu-id="754b4-130">Środowisko platformy Azure niezależne wdrożenie platformy Microsoft Azure, takiej jak AzureCloud dla usługi Azure i AzureChinaCloud dla platformy Azure obsługiwanej przez firmę 21Vianet w Chinach.</span><span class="sxs-lookup"><span data-stu-id="754b4-130">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="754b4-131">Lokalne środowiska platformy Azure można też tworzyć, korzystając z pakietu Azure i poleceń cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="754b4-131">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="754b4-132">Aby uzyskać więcej informacji, zobacz [pakiet Azure](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="754b4-132">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="754b4-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="754b4-133">-PassThru</span></span>
<span data-ttu-id="754b4-134">Zwraca wartość $True, jeśli wykonanie polecenia powiedzie się i $False, jeśli nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="754b4-134">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="754b4-135">Domyślnie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="754b4-135">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="754b4-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="754b4-136">-Profile</span></span>
<span data-ttu-id="754b4-137">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="754b4-137">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="754b4-138">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="754b4-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="754b4-139">-Obszar</span><span class="sxs-lookup"><span data-stu-id="754b4-139">-Realm</span></span>
<span data-ttu-id="754b4-140">Określa organizację w IDENTYFIKATORze organizacji.</span><span class="sxs-lookup"><span data-stu-id="754b4-140">Specifies the organization in an organizational ID.</span></span>
<span data-ttu-id="754b4-141">Na przykład jeśli logujesz się do platformy Azure jako admin@contoso.com , wartość parametru **Realm** to contoso.com.</span><span class="sxs-lookup"><span data-stu-id="754b4-141">For example, if you sign into Azure as admin@contoso.com, the value of the **Realm** parameter is contoso.com.</span></span>
<span data-ttu-id="754b4-142">Za pomocą tego parametru można zalogowanie się do witryny Azure Portal za pomocą identyfikatora organizacji.</span><span class="sxs-lookup"><span data-stu-id="754b4-142">Use this parameter when you use an organizational ID to sign into the Azure portal.</span></span>
<span data-ttu-id="754b4-143">Ten parametr nie jest wymagany w przypadku korzystania z konta Microsoft, takiego jak konto outlook.com lub live.com.</span><span class="sxs-lookup"><span data-stu-id="754b4-143">This parameter is not required when you use a Microsoft account, such as an outlook.com or live.com account.</span></span>

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

### <span data-ttu-id="754b4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="754b4-144">CommonParameters</span></span>
<span data-ttu-id="754b4-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="754b4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="754b4-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="754b4-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="754b4-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="754b4-147">INPUTS</span></span>

### <span data-ttu-id="754b4-148">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="754b4-148">None</span></span>
<span data-ttu-id="754b4-149">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="754b4-149">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="754b4-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="754b4-150">OUTPUTS</span></span>

### <span data-ttu-id="754b4-151">Brak lub system. Boolean</span><span class="sxs-lookup"><span data-stu-id="754b4-151">None or System.Boolean</span></span>
<span data-ttu-id="754b4-152">Po użyciu parametru *PassThru* to polecenie cmdlet zwraca wartość logiczną.</span><span class="sxs-lookup"><span data-stu-id="754b4-152">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="754b4-153">W przeciwnym razie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="754b4-153">Otherwise, this cmdlet does not return any output</span></span>

## <span data-ttu-id="754b4-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="754b4-154">NOTES</span></span>

## <span data-ttu-id="754b4-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="754b4-155">RELATED LINKS</span></span>

[<span data-ttu-id="754b4-156">Dodaj-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="754b4-156">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="754b4-157">Import — AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="754b4-157">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)


