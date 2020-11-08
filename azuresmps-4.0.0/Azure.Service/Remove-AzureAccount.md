---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054836"
---
# <span data-ttu-id="2ee08-101">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="2ee08-101">Remove-AzureAccount</span></span>

## <span data-ttu-id="2ee08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ee08-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee08-103">Usuwa konto platformy Azure z programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2ee08-103">Deletes an Azure account from Windows PowerShell.</span></span>

## <span data-ttu-id="2ee08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ee08-104">SYNTAX</span></span>

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ee08-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ee08-105">DESCRIPTION</span></span>
<span data-ttu-id="2ee08-106">Polecenie cmdlet **Remove-AzureAccount** usuwa konto platformy Azure i jego subskrypcje z pliku danych subskrypcji w profilu użytkownika mobilnego.</span><span class="sxs-lookup"><span data-stu-id="2ee08-106">The **Remove-AzureAccount** cmdlet deletes an Azure account and its subscriptions from the subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="2ee08-107">Nie powoduje usunięcia konta z platformy Microsoft Azure ani zmiany rzeczywistego konta w jakikolwiek sposób.</span><span class="sxs-lookup"><span data-stu-id="2ee08-107">It does not delete the account from Microsoft Azure, or change the actual account in any way.</span></span>

<span data-ttu-id="2ee08-108">Korzystanie z tego polecenia cmdlet jest bardzo podobne do logowania się z konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee08-108">Using this cmdlet is a lot like logging out of your Azure account.</span></span>
<span data-ttu-id="2ee08-109">Aby ponownie zalogować się do konta, użyj apletu **Add-AzureAccount** lub **Import-AzurePublishSettingsFile** w celu ponownego dodania konta do programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2ee08-109">And, if you want to log into the account again, use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** to add the account to Windows PowerShell again.</span></span>

<span data-ttu-id="2ee08-110">Możesz również użyć polecenia cmdlet **Remove-AzureAccount** , aby zmienić sposób, w jaki polecenia cmdlet programu Azure PowerShell będą się podpisywać do konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee08-110">You can also use **Remove-AzureAccount** cmdlet to change the way the Azure PowerShell cmdlets sign into your Azure account.</span></span>
<span data-ttu-id="2ee08-111">Jeśli konto ma certyfikat administracyjny z **Import-AzurePublishSettingsFile** i token dostępu z **dodatku Add-AzureAccount** , polecenia cmdlet programu Azure PowerShell używają tylko tokena dostępu. zignorują one certyfikat zarządzania.</span><span class="sxs-lookup"><span data-stu-id="2ee08-111">If your account has both a management certificate from **Import-AzurePublishSettingsFile** and an access token from **Add-AzureAccount** , the Azure PowerShell cmdlets use only the access token; they ignore the management certificate.</span></span>
<span data-ttu-id="2ee08-112">Aby użyć certyfikatu zarządzania, uruchom polecenie **Remove-AzureAccount**.</span><span class="sxs-lookup"><span data-stu-id="2ee08-112">To use the management certificate, run **Remove-AzureAccount**.</span></span>
<span data-ttu-id="2ee08-113">Gdy element **Remove-AzureAccount** odnajdzie certyfikat zarządzania i token dostępu, usuwa tylko token dostępu, zamiast usuwać konto.</span><span class="sxs-lookup"><span data-stu-id="2ee08-113">When **Remove-AzureAccount** finds both a management certificate and an access token, it deletes only the access token, instead of deleting the account.</span></span>
<span data-ttu-id="2ee08-114">Certyfikat zarządzania jest nadal dostępny, więc konto jest nadal dostępne dla programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2ee08-114">The management certificate is still there, so account is still available to Windows PowerShell.</span></span>

<span data-ttu-id="2ee08-115">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee08-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2ee08-116">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2ee08-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="2ee08-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ee08-117">EXAMPLES</span></span>

### <span data-ttu-id="2ee08-118">Przykład 1. Usuń konto</span><span class="sxs-lookup"><span data-stu-id="2ee08-118">Example 1: Remove an account</span></span>
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

<span data-ttu-id="2ee08-119">To polecenie usuwa admin@contoso.com z pliku danych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2ee08-119">This command removes the admin@contoso.com from your subscription data file.</span></span>
<span data-ttu-id="2ee08-120">Po zakończeniu polecenia konto nie jest już dostępne w programie Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2ee08-120">When the command completes, the account is no longer available to Windows PowerShell.</span></span>

## <span data-ttu-id="2ee08-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ee08-121">PARAMETERS</span></span>

### <span data-ttu-id="2ee08-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2ee08-122">-Force</span></span>
<span data-ttu-id="2ee08-123">Pomija monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2ee08-123">Suppresses the confirmation prompt.</span></span>
<span data-ttu-id="2ee08-124">Domyślnie polecenie **Remove-AzureAccount** wyświetla monit przed usunięciem konta z programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2ee08-124">By default, **Remove-AzureAccount** prompts you before removing the account from Windows PowerShell.</span></span>

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

### <span data-ttu-id="2ee08-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2ee08-125">-Name</span></span>
<span data-ttu-id="2ee08-126">Określa nazwę konta, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="2ee08-126">Specifies the name of the account to remove.</span></span>
<span data-ttu-id="2ee08-127">W wartości parametru jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="2ee08-127">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="2ee08-128">Symbole wieloznaczne nie są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="2ee08-128">Wildcard characters are not supported.</span></span>

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

### <span data-ttu-id="2ee08-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ee08-129">-PassThru</span></span>
<span data-ttu-id="2ee08-130">Zwraca wartość $True, jeśli wykonanie polecenia powiedzie się i $False, jeśli nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="2ee08-130">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="2ee08-131">Domyślnie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2ee08-131">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="2ee08-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="2ee08-132">-Profile</span></span>
<span data-ttu-id="2ee08-133">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ee08-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2ee08-134">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2ee08-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ee08-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ee08-135">-Confirm</span></span>
<span data-ttu-id="2ee08-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ee08-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee08-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ee08-137">-WhatIf</span></span>
<span data-ttu-id="2ee08-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ee08-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ee08-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2ee08-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee08-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee08-140">CommonParameters</span></span>
<span data-ttu-id="2ee08-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee08-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee08-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee08-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee08-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ee08-143">INPUTS</span></span>

### <span data-ttu-id="2ee08-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2ee08-144">None</span></span>
<span data-ttu-id="2ee08-145">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="2ee08-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="2ee08-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ee08-146">OUTPUTS</span></span>

### <span data-ttu-id="2ee08-147">Brak lub system. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ee08-147">None or System.Boolean</span></span>
<span data-ttu-id="2ee08-148">W przypadku użycia parametru *PassThru* to polecenie cmdlet zwraca wartość logiczną.</span><span class="sxs-lookup"><span data-stu-id="2ee08-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="2ee08-149">W przeciwnym razie nie zwróci żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2ee08-149">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="2ee08-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ee08-150">NOTES</span></span>

## <span data-ttu-id="2ee08-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ee08-151">RELATED LINKS</span></span>

[<span data-ttu-id="2ee08-152">Dodaj-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="2ee08-152">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="2ee08-153">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="2ee08-153">Get-AzureAccount</span></span>](./Get-AzureAccount.md)


