---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 69619b9f5ddd54e0d307a096cc967c307d1f36d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527921"
---
# <span data-ttu-id="43a84-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="43a84-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="43a84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43a84-102">SYNOPSIS</span></span>
<span data-ttu-id="43a84-103">Ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="43a84-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43a84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43a84-104">SYNTAX</span></span>

### <span data-ttu-id="43a84-105">Rozwinięty (domyślny)</span><span class="sxs-lookup"><span data-stu-id="43a84-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43a84-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="43a84-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43a84-107">Opis</span><span class="sxs-lookup"><span data-stu-id="43a84-107">DESCRIPTION</span></span>
<span data-ttu-id="43a84-108">Polecenie cmdlet Set-AzureKeyVaultCertificateIssuer ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="43a84-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="43a84-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43a84-109">EXAMPLES</span></span>

### <span data-ttu-id="43a84-110">Przykład 1: Ustawianie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="43a84-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="43a84-111">To polecenie ustawia właściwości dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="43a84-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="43a84-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43a84-112">PARAMETERS</span></span>

### <span data-ttu-id="43a84-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="43a84-113">-AccountId</span></span>
<span data-ttu-id="43a84-114">Określa identyfikator konta dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="43a84-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a84-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="43a84-115">-ApiKey</span></span>
<span data-ttu-id="43a84-116">Określa klucz interfejsu API dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="43a84-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a84-117">-DefaultProfile</span></span>
<span data-ttu-id="43a84-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="43a84-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a84-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43a84-119">-InputObject</span></span>
<span data-ttu-id="43a84-120">Określa wystawcę certyfikatu do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="43a84-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43a84-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="43a84-121">-IssuerProvider</span></span>
<span data-ttu-id="43a84-122">Określa typ wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="43a84-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a84-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43a84-123">-Name</span></span>
<span data-ttu-id="43a84-124">Określa nazwę emitenta.</span><span class="sxs-lookup"><span data-stu-id="43a84-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a84-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="43a84-125">-OrganizationDetails</span></span>
<span data-ttu-id="43a84-126">Szczegóły organizacji, które mają być używane z wystawcą.</span><span class="sxs-lookup"><span data-stu-id="43a84-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43a84-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43a84-127">-PassThru</span></span>
<span data-ttu-id="43a84-128">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="43a84-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="43a84-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="43a84-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a84-130">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="43a84-130">-VaultName</span></span>
<span data-ttu-id="43a84-131">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="43a84-131">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a84-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43a84-132">-Confirm</span></span>
<span data-ttu-id="43a84-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43a84-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a84-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43a84-134">-WhatIf</span></span>
<span data-ttu-id="43a84-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43a84-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43a84-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="43a84-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a84-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a84-137">CommonParameters</span></span>
<span data-ttu-id="43a84-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43a84-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a84-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43a84-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a84-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43a84-140">INPUTS</span></span>

### <span data-ttu-id="43a84-141">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="43a84-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>
<span data-ttu-id="43a84-142">Parametry: OrganizationDetails (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43a84-142">Parameters: OrganizationDetails (ByValue)</span></span>

### <span data-ttu-id="43a84-143">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="43a84-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>
<span data-ttu-id="43a84-144">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43a84-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="43a84-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43a84-145">OUTPUTS</span></span>

### <span data-ttu-id="43a84-146">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="43a84-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="43a84-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43a84-147">NOTES</span></span>

## <span data-ttu-id="43a84-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43a84-148">RELATED LINKS</span></span>

[<span data-ttu-id="43a84-149">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="43a84-149">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="43a84-150">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="43a84-150">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

