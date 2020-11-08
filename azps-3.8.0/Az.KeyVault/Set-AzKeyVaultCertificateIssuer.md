---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 332a4251919356fa276ce281219f91bf470ba6db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051510"
---
# <span data-ttu-id="03b5c-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="03b5c-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="03b5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="03b5c-103">Ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="03b5c-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="03b5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03b5c-104">SYNTAX</span></span>

### <span data-ttu-id="03b5c-105">Rozwinięty (domyślny)</span><span class="sxs-lookup"><span data-stu-id="03b5c-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03b5c-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="03b5c-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03b5c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="03b5c-107">DESCRIPTION</span></span>
<span data-ttu-id="03b5c-108">Polecenie cmdlet Set-AzKeyVaultCertificateIssuer ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="03b5c-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="03b5c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03b5c-109">EXAMPLES</span></span>

### <span data-ttu-id="03b5c-110">Przykład 1: Ustawianie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="03b5c-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="03b5c-111">To polecenie ustawia właściwości dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="03b5c-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="03b5c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03b5c-112">PARAMETERS</span></span>

### <span data-ttu-id="03b5c-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="03b5c-113">-AccountId</span></span>
<span data-ttu-id="03b5c-114">Określa identyfikator konta dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="03b5c-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="03b5c-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="03b5c-115">-ApiKey</span></span>
<span data-ttu-id="03b5c-116">Określa klucz interfejsu API dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="03b5c-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="03b5c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b5c-117">-DefaultProfile</span></span>
<span data-ttu-id="03b5c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="03b5c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b5c-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03b5c-119">-InputObject</span></span>
<span data-ttu-id="03b5c-120">Określa wystawcę certyfikatu do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="03b5c-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="03b5c-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="03b5c-121">-IssuerProvider</span></span>
<span data-ttu-id="03b5c-122">Określa typ wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="03b5c-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="03b5c-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03b5c-123">-Name</span></span>
<span data-ttu-id="03b5c-124">Określa nazwę emitenta.</span><span class="sxs-lookup"><span data-stu-id="03b5c-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="03b5c-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="03b5c-125">-OrganizationDetails</span></span>
<span data-ttu-id="03b5c-126">Szczegóły organizacji, które mają być używane z wystawcą.</span><span class="sxs-lookup"><span data-stu-id="03b5c-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="03b5c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03b5c-127">-PassThru</span></span>
<span data-ttu-id="03b5c-128">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="03b5c-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03b5c-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="03b5c-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03b5c-130">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="03b5c-130">-VaultName</span></span>
<span data-ttu-id="03b5c-131">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="03b5c-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="03b5c-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03b5c-132">-Confirm</span></span>
<span data-ttu-id="03b5c-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03b5c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03b5c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03b5c-134">-WhatIf</span></span>
<span data-ttu-id="03b5c-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03b5c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03b5c-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03b5c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03b5c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b5c-137">CommonParameters</span></span>
<span data-ttu-id="03b5c-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b5c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b5c-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03b5c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b5c-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03b5c-140">INPUTS</span></span>

### <span data-ttu-id="03b5c-141">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="03b5c-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="03b5c-142">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="03b5c-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="03b5c-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03b5c-143">OUTPUTS</span></span>

### <span data-ttu-id="03b5c-144">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="03b5c-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="03b5c-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03b5c-145">NOTES</span></span>

## <span data-ttu-id="03b5c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03b5c-146">RELATED LINKS</span></span>

[<span data-ttu-id="03b5c-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="03b5c-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="03b5c-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="03b5c-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

