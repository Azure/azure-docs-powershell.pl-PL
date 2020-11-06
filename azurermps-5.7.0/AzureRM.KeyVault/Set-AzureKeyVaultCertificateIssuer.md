---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 2a79f4bb555576414b4ed14c06ee0050133e139d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553671"
---
# <span data-ttu-id="404ec-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="404ec-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="404ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="404ec-102">SYNOPSIS</span></span>
<span data-ttu-id="404ec-103">Ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="404ec-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="404ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="404ec-104">SYNTAX</span></span>

### <span data-ttu-id="404ec-105">Rozwinięty (domyślny)</span><span class="sxs-lookup"><span data-stu-id="404ec-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="404ec-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="404ec-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="404ec-107">Opis</span><span class="sxs-lookup"><span data-stu-id="404ec-107">DESCRIPTION</span></span>
<span data-ttu-id="404ec-108">Polecenie cmdlet Set-AzureKeyVaultCertificateIssuer ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="404ec-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="404ec-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="404ec-109">EXAMPLES</span></span>

### <span data-ttu-id="404ec-110">Przykład 1: Ustawianie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="404ec-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="404ec-111">To polecenie ustawia właściwości dla wystawcy certyfikatu, a następnie zapisuje je w zmiennej $Issuer.</span><span class="sxs-lookup"><span data-stu-id="404ec-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="404ec-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="404ec-112">PARAMETERS</span></span>

### <span data-ttu-id="404ec-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="404ec-113">-AccountId</span></span>
<span data-ttu-id="404ec-114">Określa identyfikator konta dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="404ec-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ec-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="404ec-115">-ApiKey</span></span>
<span data-ttu-id="404ec-116">Określa klucz interfejsu API dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="404ec-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="404ec-117">-DefaultProfile</span></span>
<span data-ttu-id="404ec-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="404ec-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404ec-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="404ec-119">-InputObject</span></span>
<span data-ttu-id="404ec-120">Określa wystawcę certyfikatu do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="404ec-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="404ec-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="404ec-121">-IssuerProvider</span></span>
<span data-ttu-id="404ec-122">Określa typ wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="404ec-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ec-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="404ec-123">-Name</span></span>
<span data-ttu-id="404ec-124">Określa nazwę emitenta.</span><span class="sxs-lookup"><span data-stu-id="404ec-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ec-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="404ec-125">-OrganizationDetails</span></span>
<span data-ttu-id="404ec-126">Szczegóły organizacji, które mają być używane z wystawcą.</span><span class="sxs-lookup"><span data-stu-id="404ec-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ec-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="404ec-127">-PassThru</span></span>
<span data-ttu-id="404ec-128">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="404ec-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="404ec-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="404ec-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="404ec-130">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="404ec-130">-VaultName</span></span>
<span data-ttu-id="404ec-131">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="404ec-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="404ec-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="404ec-132">-Confirm</span></span>
<span data-ttu-id="404ec-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="404ec-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404ec-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="404ec-134">-WhatIf</span></span>
<span data-ttu-id="404ec-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="404ec-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="404ec-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="404ec-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404ec-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="404ec-137">CommonParameters</span></span>
<span data-ttu-id="404ec-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="404ec-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="404ec-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="404ec-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="404ec-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="404ec-140">INPUTS</span></span>

### <span data-ttu-id="404ec-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="404ec-141">None</span></span>
<span data-ttu-id="404ec-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="404ec-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="404ec-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="404ec-143">OUTPUTS</span></span>

### <span data-ttu-id="404ec-144">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="404ec-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="404ec-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="404ec-145">NOTES</span></span>

## <span data-ttu-id="404ec-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="404ec-146">RELATED LINKS</span></span>

[<span data-ttu-id="404ec-147">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="404ec-147">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="404ec-148">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="404ec-148">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

