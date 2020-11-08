---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A6D5C40-2532-4FD1-A74F-16725CAD8EDD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29d049dbdce93102411a875cfaef8e5fb9c719b6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055361"
---
# <span data-ttu-id="72e61-101">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="72e61-101">Add-AzureCertificate</span></span>

## <span data-ttu-id="72e61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72e61-102">SYNOPSIS</span></span>
<span data-ttu-id="72e61-103">Wysyła certyfikat do usługi w chmurze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="72e61-103">Uploads a certificate to an Azure cloud service.</span></span>

## <span data-ttu-id="72e61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72e61-104">SYNTAX</span></span>

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="72e61-105">Opis</span><span class="sxs-lookup"><span data-stu-id="72e61-105">DESCRIPTION</span></span>
<span data-ttu-id="72e61-106">Polecenie cmdlet **Add-AzureCertificate** umożliwia przekazywanie certyfikatu dla usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="72e61-106">The **Add-AzureCertificate** cmdlet uploads a certificate for an Azure service.</span></span>

## <span data-ttu-id="72e61-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72e61-107">EXAMPLES</span></span>

### <span data-ttu-id="72e61-108">Przykład 1: przekazywanie certyfikatu i hasła</span><span class="sxs-lookup"><span data-stu-id="72e61-108">Example 1: Upload a certificate and password</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

<span data-ttu-id="72e61-109">To polecenie umożliwia przekazywanie pliku certyfikatu ContosoCertificate. pfx do usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="72e61-109">This command uploads the certificate file ContosoCertificate.pfx to a cloud service.</span></span>
<span data-ttu-id="72e61-110">Polecenie Określa hasło dla certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="72e61-110">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="72e61-111">Przykład 2: przekazywanie pliku certyfikatu</span><span class="sxs-lookup"><span data-stu-id="72e61-111">Example 2: Upload a certificate file</span></span>
```
PS C:\> Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

<span data-ttu-id="72e61-112">To polecenie wysyła plik certyfikatu ContosoCertificate. cer do usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="72e61-112">This command uploads the certificate file ContosoCertificate.cer to a cloud service.</span></span>
<span data-ttu-id="72e61-113">Polecenie Określa hasło dla certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="72e61-113">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="72e61-114">Przykład 3: przekazywanie obiektu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="72e61-114">Example 3: Upload a certificate object</span></span>
```
PS C:\> $Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

<span data-ttu-id="72e61-115">Pierwsze polecenie pobiera certyfikat z mojego sklepu użytkownika przy użyciu polecenia cmdlet programu Windows PowerShell Core **-Item** .</span><span class="sxs-lookup"><span data-stu-id="72e61-115">The first command gets a certificate from the MY store of a user by using the Windows PowerShell core **Get-Item** cmdlet.</span></span>
<span data-ttu-id="72e61-116">Polecenie zapisuje certyfikat w zmiennej $Certificate.</span><span class="sxs-lookup"><span data-stu-id="72e61-116">The command stores the certificate in the $Certificate variable.</span></span>

<span data-ttu-id="72e61-117">Drugie polecenie wysyła certyfikat w $certificate do usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="72e61-117">The second command uploads the certificate in $certificate to a cloud service.</span></span>

## <span data-ttu-id="72e61-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72e61-118">PARAMETERS</span></span>

### <span data-ttu-id="72e61-119">-CertToDeploy</span><span class="sxs-lookup"><span data-stu-id="72e61-119">-CertToDeploy</span></span>
<span data-ttu-id="72e61-120">Określa certyfikat, który należy wdrożyć.</span><span class="sxs-lookup"><span data-stu-id="72e61-120">Specifies the certificate to deploy.</span></span>
<span data-ttu-id="72e61-121">Możesz określić pełną ścieżkę do pliku certyfikatu, na przykład plik z rozszerzeniem \*. cer lub \*.</span><span class="sxs-lookup"><span data-stu-id="72e61-121">You can specify the full path of a certificate file, such as a file that has a \*.cer or \*.</span></span>
<span data-ttu-id="72e61-122">rozszerzenie nazwy pliku PFX lub obiekt certyfikatu X. 509.</span><span class="sxs-lookup"><span data-stu-id="72e61-122">pfx file name extension, or an X.509 Certificate object.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e61-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="72e61-123">-InformationAction</span></span>
<span data-ttu-id="72e61-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="72e61-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="72e61-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="72e61-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="72e61-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="72e61-126">Continue</span></span>
- <span data-ttu-id="72e61-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="72e61-127">Ignore</span></span>
- <span data-ttu-id="72e61-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="72e61-128">Inquire</span></span>
- <span data-ttu-id="72e61-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="72e61-129">SilentlyContinue</span></span>
- <span data-ttu-id="72e61-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="72e61-130">Stop</span></span>
- <span data-ttu-id="72e61-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="72e61-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e61-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="72e61-132">-InformationVariable</span></span>
<span data-ttu-id="72e61-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="72e61-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e61-134">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="72e61-134">-Password</span></span>
<span data-ttu-id="72e61-135">Określa hasło certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="72e61-135">Specifies the certificate password.</span></span>

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

### <span data-ttu-id="72e61-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="72e61-136">-Profile</span></span>
<span data-ttu-id="72e61-137">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72e61-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="72e61-138">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="72e61-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="72e61-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="72e61-139">-ServiceName</span></span>
<span data-ttu-id="72e61-140">Określa nazwę usługi platformy Azure, z którą to polecenie cmdlet dodaje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="72e61-140">Specifies the name of the Azure service to which this cmdlet adds a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72e61-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e61-141">CommonParameters</span></span>
<span data-ttu-id="72e61-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e61-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e61-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e61-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e61-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72e61-144">INPUTS</span></span>

## <span data-ttu-id="72e61-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72e61-145">OUTPUTS</span></span>

### <span data-ttu-id="72e61-146">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="72e61-146">ManagementOperationContext</span></span>

## <span data-ttu-id="72e61-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72e61-147">NOTES</span></span>

## <span data-ttu-id="72e61-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72e61-148">RELATED LINKS</span></span>

[<span data-ttu-id="72e61-149">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="72e61-149">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="72e61-150">Nowe — AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="72e61-150">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="72e61-151">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="72e61-151">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


