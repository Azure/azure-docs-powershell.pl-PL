---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055362"
---
# <span data-ttu-id="1601a-101">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="1601a-101">Add-AzureAccount</span></span>

## <span data-ttu-id="1601a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1601a-102">SYNOPSIS</span></span>
<span data-ttu-id="1601a-103">Dodaje konto platformy Azure do programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1601a-103">Adds the Azure account to Windows PowerShell.</span></span>

## <span data-ttu-id="1601a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1601a-104">SYNTAX</span></span>

### <span data-ttu-id="1601a-105">Użytkownik (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1601a-105">User (Default)</span></span>
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1601a-106">Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="1601a-106">ServicePrincipal</span></span>
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1601a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1601a-107">DESCRIPTION</span></span>
<span data-ttu-id="1601a-108">Polecenie cmdlet **Add-AzureAccount** umożliwia udostępnianie konta platformy Azure i jego subskrypcji w programie Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1601a-108">The **Add-AzureAccount** cmdlet makes your Azure account and its subscriptions available in Windows PowerShell.</span></span>
<span data-ttu-id="1601a-109">Przypomina to logowanie się do konta platformy Azure w programie Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1601a-109">It's like logging into your Azure account in Windows PowerShell.</span></span>
<span data-ttu-id="1601a-110">Aby wylogować się z konta, użyj polecenia cmdlet **Remove-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="1601a-110">To log out of the account, use the **Remove-AzureAccount** cmdlet.</span></span>

<span data-ttu-id="1601a-111">**Dodatek Add-AzureAccount** pobiera informacje o koncie platformy Azure i zapisuje je w pliku danych subskrypcji w profilu użytkownika mobilnego.</span><span class="sxs-lookup"><span data-stu-id="1601a-111">**Add-AzureAccount** downloads information about your Azure account and saves it in a subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="1601a-112">Jest również dostępny token dostępu, który umożliwia programowi Windows PowerShell uzyskiwanie dostępu do konta platformy Azure w Twoim imieniu.</span><span class="sxs-lookup"><span data-stu-id="1601a-112">It also gets an access token that allows Windows PowerShell to access your Azure account on your behalf.</span></span>
<span data-ttu-id="1601a-113">Po zakończeniu wykonywania polecenia możesz zarządzać kontem platformy Azure w programie Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1601a-113">When the command completes, you can manage your Azure account in Windows PowerShell.</span></span>

<span data-ttu-id="1601a-114">Dostępne są dwie różne metody tworzenia konta platformy Azure w programie Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1601a-114">There are two different ways to make your Azure account available to Windows PowerShell.</span></span>
<span data-ttu-id="1601a-115">Możesz użyć polecenia cmdlet **Add-AzureAccount** , które używa tokenów dostępu do uwierzytelniania w usłudze Azure Active Directory (Azure AD) lub **importu-AzurePublishSettingsFile** , który używa certyfikatu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="1601a-115">You can use the **Add-AzureAccount** cmdlet, which uses Azure Active Directory (Azure AD) authentication access tokens, or **Import-AzurePublishSettingsFile** , which uses a management certificate.</span></span>
<span data-ttu-id="1601a-116">Aby uzyskać wskazówki dotyczące metody, której należy użyć, zobacz [jak: Nawiązywanie połączenia z subskrypcją](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .</span><span class="sxs-lookup"><span data-stu-id="1601a-116">For guidance on which method to use, see [How to: Connect to your subscription](https://azure.microsoft.com/documentation/articles/install-configure-powershell) (https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect).</span></span>

<span data-ttu-id="1601a-117">Po uruchomieniu polecenia **Add-AzureAccount** zostanie wyświetlone interaktywne okno, w którym jest wyświetlany monit o zalogowanie się do konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1601a-117">When you run **Add-AzureAccount** , it displays an interactive window that prompts you to sign into your Azure account.</span></span>
<span data-ttu-id="1601a-118">To logowanie jest ważne do czasu wygaśnięcia tokenu dostępu.</span><span class="sxs-lookup"><span data-stu-id="1601a-118">This sign-in is valid until the access token expires.</span></span>
<span data-ttu-id="1601a-119">Gdy wygaśnie, polecenia cmdlet wymagające dostępu do konta wymagają ponownego uruchomienia polecenia **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="1601a-119">When it expires, cmdlets that require access to your account prompt you to run **Add-AzureAccount** again.</span></span>

<span data-ttu-id="1601a-120">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1601a-120">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1601a-121">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1601a-121">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="1601a-122">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1601a-122">EXAMPLES</span></span>

### <span data-ttu-id="1601a-123">Przykład 1: Dodawanie konta</span><span class="sxs-lookup"><span data-stu-id="1601a-123">Example 1: Add an account</span></span>
```
PS C:\> Add-AzureAccount
```

<span data-ttu-id="1601a-124">To polecenie dodaje konto platformy Azure do programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1601a-124">This command adds an Azure account to Windows PowerShell.</span></span>
<span data-ttu-id="1601a-125">Po uruchomieniu polecenia w systemie Windows zostanie wyświetlony monit o podanie nazwy użytkownika i hasła do konta.</span><span class="sxs-lookup"><span data-stu-id="1601a-125">When you run the command, a windows pops up to request the user name and password of the account.</span></span>

### <span data-ttu-id="1601a-126">Przykład 2: używanie alternatywnego pliku danych subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1601a-126">Example 2: Use an alternate subscription data file</span></span>
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

<span data-ttu-id="1601a-127">To polecenie używa parametru **SubscriptionDataFile** w celu kierowania polecenia **Add-AzureAccount** w celu przechowywania danych konta w pliku C:\Testing\SDF.xml, a nie w pliku domyślnym.</span><span class="sxs-lookup"><span data-stu-id="1601a-127">This command uses the **SubscriptionDataFile** parameter to direct **Add-AzureAccount** to store the account data in the C:\Testing\SDF.xml file, instead of the default file.</span></span>

## <span data-ttu-id="1601a-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1601a-128">PARAMETERS</span></span>

### <span data-ttu-id="1601a-129">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="1601a-129">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1601a-130">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="1601a-130">-Environment</span></span>
<span data-ttu-id="1601a-131">Określa środowisko Azure.</span><span class="sxs-lookup"><span data-stu-id="1601a-131">Specifies an Azure environment.</span></span>

<span data-ttu-id="1601a-132">Środowisko platformy Azure niezależne wdrożenie platformy Microsoft Azure, takiej jak AzureCloud dla usługi Azure i AzureChinaCloud dla platformy Azure obsługiwanej przez firmę 21Vianet w Chinach.</span><span class="sxs-lookup"><span data-stu-id="1601a-132">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="1601a-133">Lokalne środowiska platformy Azure można też tworzyć, korzystając z pakietu Azure i poleceń cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="1601a-133">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="1601a-134">Aby uzyskać więcej informacji, zobacz [pakiet Azure](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1601a-134">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="1601a-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="1601a-135">-Profile</span></span>
<span data-ttu-id="1601a-136">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1601a-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1601a-137">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1601a-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1601a-138">-Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="1601a-138">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1601a-139">-Dzierżawca</span><span class="sxs-lookup"><span data-stu-id="1601a-139">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1601a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1601a-140">CommonParameters</span></span>
<span data-ttu-id="1601a-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1601a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1601a-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1601a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1601a-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1601a-143">INPUTS</span></span>

### <span data-ttu-id="1601a-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1601a-144">None</span></span>
<span data-ttu-id="1601a-145">Nie można popotokować danych wejściowych tego polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="1601a-145">You cannot pipe input to this cmdlet</span></span>

## <span data-ttu-id="1601a-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1601a-146">OUTPUTS</span></span>

### <span data-ttu-id="1601a-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1601a-147">None</span></span>
<span data-ttu-id="1601a-148">To polecenie cmdlet nie zwraca żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1601a-148">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="1601a-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1601a-149">NOTES</span></span>
* <span data-ttu-id="1601a-150">**Dodatek Add-AzureAccount** (i metoda uwierzytelniania usługi Azure AD) ma pierwszeństwo przed **importem-AzurePublishSettings** (i metodą certyfikatu zarządzania).</span><span class="sxs-lookup"><span data-stu-id="1601a-150">**Add-AzureAccount** (and the Azure AD authentication method) takes precedence over **Import-AzurePublishSettings** (and the management certificate method).</span></span> <span data-ttu-id="1601a-151">Jeśli na koncie jest używane polecenie **Add-AzureAccount** , zostanie użyta metoda uwierzytelniania usługi Azure AD, a certyfikat zarządzania jest ignorowany.</span><span class="sxs-lookup"><span data-stu-id="1601a-151">If you use **Add-AzureAccount** even once on your account, the Azure AD authentication method is used and the management certificate is ignored.</span></span> <span data-ttu-id="1601a-152">Aby usunąć token usługi Azure AD i przywrócić metodę certyfikatu zarządzania, użyj polecenia cmdlet **Remove-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="1601a-152">To remove the Azure AD token and restore the management certificate method, use the **Remove-AzureAccount** cmdlet.</span></span> <span data-ttu-id="1601a-153">Aby uzyskać więcej informacji, wpisz ciąg: **Get-Help Remove-AzureAccount**.</span><span class="sxs-lookup"><span data-stu-id="1601a-153">For more information, type: **Get-Help Remove-AzureAccount**.</span></span>
* <span data-ttu-id="1601a-154">Błąd — Twoje poświadczenia wygasły.</span><span class="sxs-lookup"><span data-stu-id="1601a-154">The error, "Your credentials have expired.</span></span> <span data-ttu-id="1601a-155">Użyj Add-AzureAccount, aby zalogować się ponownie.</span><span class="sxs-lookup"><span data-stu-id="1601a-155">Please use Add-AzureAccount to log in again."</span></span> <span data-ttu-id="1601a-156">wskazuje, że token dostępu wygasł i program Windows PowerShell nie może uzyskać dostępu do konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1601a-156">indicates that your access token is expired and Windows PowerShell cannot access your Azure account.</span></span> <span data-ttu-id="1601a-157">Aby przywrócić dostęp do konta, ponownie uruchom polecenie **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="1601a-157">To restore access to your account, run **Add-AzureAccount** again.</span></span>
* <span data-ttu-id="1601a-158">Polecenia cmdlet konta i subskrypcji usługi Azure PowerShell uzyskują dane z pliku danych subskrypcji, a nie z konta usługi Live Azure.</span><span class="sxs-lookup"><span data-stu-id="1601a-158">The Azure PowerShell account and subscription cmdlets get their data from the  subscription data file, not from the live Azure account.</span></span> <span data-ttu-id="1601a-159">Jeśli zmienisz swoje konto lub abonamenty poza programem Windows PowerShell, na przykład za pomocą portalu zarządzania Azure, ponownie uruchom **dodatek Add-AzureAccount** , aby odświeżyć plik danych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1601a-159">If you change your account or subscriptions outside of Windows PowerShell, such as by using the Azure Management Portal, run **Add-AzureAccount** again to refresh the subscription data file.</span></span>

## <span data-ttu-id="1601a-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1601a-160">RELATED LINKS</span></span>

[<span data-ttu-id="1601a-161">Dodaj-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="1601a-161">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="1601a-162">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="1601a-162">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="1601a-163">Import — AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1601a-163">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="1601a-164">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="1601a-164">Get-AzureAccount</span></span>](./Get-AzureAccount.md)

[<span data-ttu-id="1601a-165">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="1601a-165">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


