---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055227"
---
# <span data-ttu-id="f9e93-101">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f9e93-101">Import-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="f9e93-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9e93-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e93-103">Importuje plik ustawień publikowania, który umożliwia zarządzanie kontami platformy Azure w programie Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f9e93-103">Imports a publish settings file that lets you manage your Azure accounts in Windows PowerShell.</span></span>

## <span data-ttu-id="f9e93-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9e93-104">SYNTAX</span></span>

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f9e93-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f9e93-105">DESCRIPTION</span></span>
<span data-ttu-id="f9e93-106">Polecenie cmdlet **Import-AzurePublishSettingsFile** importuje plik ustawień publikowania (\*. publishsettings), który zawiera informacje na temat kont platformy Azure i zapisuje plik danych abonamentu na komputerze.</span><span class="sxs-lookup"><span data-stu-id="f9e93-106">The **Import-AzurePublishSettingsFile** cmdlet imports a publish settings file (\*.publishsettings) that contains information about your Azure accounts and saves a subscription data file on your computer.</span></span>
<span data-ttu-id="f9e93-107">Po zakończeniu działania polecenia cmdlet możesz zarządzać kontami platformy Azure w programie Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f9e93-107">When the cmdlet completes, you can manage your Azure accounts in Windows PowerShell.</span></span>

<span data-ttu-id="f9e93-108">Przed uruchomieniem programu **Import-AzurePublishSettingsFile** Uruchom polecenie **Get-AzurePublishSettingsFile** , które umożliwia pobranie i zapisanie pliku ustawień publikowania w celu jego zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="f9e93-108">Before running **Import-AzurePublishSettingsFile** , run **Get-AzurePublishSettingsFile** , which downloads and saves the publish settings file so you can import it.</span></span>

<span data-ttu-id="f9e93-109">Aby konto platformy Azure było dostępne dla programu Windows PowerShell, możesz użyć pliku ustawień publikowania lub polecenia cmdlet **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="f9e93-109">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="f9e93-110">Publikowanie plików ustawień umożliwia przygotowywanie sesji z wyprzedzeniem, aby można było uruchamiać skrypty i zadania w tle bez opieki.</span><span class="sxs-lookup"><span data-stu-id="f9e93-110">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="f9e93-111">Jednak nie wszystkie usługi obsługują pliki ustawień publikowania.</span><span class="sxs-lookup"><span data-stu-id="f9e93-111">However, not all services support publish settings files.</span></span>
<span data-ttu-id="f9e93-112">Na przykład moduł **AzureResourceManager** nie obsługuje plików ustawień publikowania.</span><span class="sxs-lookup"><span data-stu-id="f9e93-112">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="f9e93-113">**Uwaga dotycząca zabezpieczeń:** Pliki ustawień publikowania zawierają certyfikat zarządzania, który jest kodowany, ale nie jest szyfrowany.</span><span class="sxs-lookup"><span data-stu-id="f9e93-113">**Security Note:** Publish settings files contain a management certificate that is encoded, but not encrypted.</span></span>
<span data-ttu-id="f9e93-114">Jeśli Złośliwi użytkownicy uzyskują dostęp do pliku ustawień publikowania, mogą oni mieć możliwość edytowania, tworzenia i usuwania usług platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e93-114">If  malicious users access your publish settings file,  they might be able to edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="f9e93-115">Zgodnie z najważniejszymi wskazówkami dotyczącymi zabezpieczeń Zapisz plik w lokalizacji w folderze pobrane pliki lub dokumenty, a następnie usuń go po użyciu polecenia cmdlet **importu-AzurePublishSettingsFile** w celu zaimportowania ustawień.</span><span class="sxs-lookup"><span data-stu-id="f9e93-115">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

## <span data-ttu-id="f9e93-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9e93-116">EXAMPLES</span></span>

### <span data-ttu-id="f9e93-117">Przykład 1: Importowanie pliku</span><span class="sxs-lookup"><span data-stu-id="f9e93-117">Example 1: Import a file</span></span>
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

<span data-ttu-id="f9e93-118">To polecenie umożliwia zaimportowanie pliku "C:\Temp\MyAccount.publishsettings".</span><span class="sxs-lookup"><span data-stu-id="f9e93-118">This command imports the "C:\Temp\MyAccount.publishsettings" file.</span></span>

## <span data-ttu-id="f9e93-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9e93-119">PARAMETERS</span></span>

### <span data-ttu-id="f9e93-120">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="f9e93-120">-Environment</span></span>
<span data-ttu-id="f9e93-121">Określa środowisko Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e93-121">Specifies an Azure environment.</span></span>

<span data-ttu-id="f9e93-122">Środowisko platformy Azure niezależne wdrożenie platformy Microsoft Azure, takiej jak AzureCloud dla usługi Azure i AzureChinaCloud dla platformy Azure obsługiwanej przez firmę 21Vianet w Chinach.</span><span class="sxs-lookup"><span data-stu-id="f9e93-122">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="f9e93-123">Lokalne środowiska platformy Azure można też tworzyć, korzystając z pakietu Azure i poleceń cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="f9e93-123">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="f9e93-124">Aby uzyskać więcej informacji, zobacz [pakiet Azure](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f9e93-124">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="f9e93-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="f9e93-125">-Profile</span></span>
<span data-ttu-id="f9e93-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9e93-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f9e93-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f9e93-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f9e93-128">-PublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f9e93-128">-PublishSettingsFile</span></span>
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

### <span data-ttu-id="f9e93-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e93-129">CommonParameters</span></span>
<span data-ttu-id="f9e93-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9e93-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e93-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9e93-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e93-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9e93-132">INPUTS</span></span>

### <span data-ttu-id="f9e93-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f9e93-133">None</span></span>
<span data-ttu-id="f9e93-134">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="f9e93-134">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="f9e93-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9e93-135">OUTPUTS</span></span>

### <span data-ttu-id="f9e93-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f9e93-136">None</span></span>
<span data-ttu-id="f9e93-137">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f9e93-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f9e93-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9e93-138">NOTES</span></span>
* <span data-ttu-id="f9e93-139">"Plik ustawień publikowania" to plik XML z rozszerzeniem nazwy pliku publishsettings.</span><span class="sxs-lookup"><span data-stu-id="f9e93-139">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span> <span data-ttu-id="f9e93-140">Plik zawiera zakodowany certyfikat, który zawiera poświadczenia zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e93-140">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span> <span data-ttu-id="f9e93-141">Po zaimportowaniu pliku usuń go, aby uniknąć zagrożenia bezpieczeństwa.</span><span class="sxs-lookup"><span data-stu-id="f9e93-141">After you import this file, delete it to avoid security risks.</span></span>
* <span data-ttu-id="f9e93-142">"Plik danych abonamentu" to plik XML, który można bezpiecznie zapisać na komputerze.</span><span class="sxs-lookup"><span data-stu-id="f9e93-142">A "subscription data file" is an XML file that can be saved on your computer safely.</span></span> <span data-ttu-id="f9e93-143">Domyślnie jest on zapisany w profilu użytkownika mobilnego ($home/AppData/Roaming).</span><span class="sxs-lookup"><span data-stu-id="f9e93-143">By default, it's saved in your roaming user profile ($home/AppData/Roaming).</span></span>

## <span data-ttu-id="f9e93-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9e93-144">RELATED LINKS</span></span>

[<span data-ttu-id="f9e93-145">Jak zainstalować i skonfigurować środowisko Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9e93-145">How to Install and Configure Azure PowerShell</span></span>](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[<span data-ttu-id="f9e93-146">Dodaj-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="f9e93-146">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="f9e93-147">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f9e93-147">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)


