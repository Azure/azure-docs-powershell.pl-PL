---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 33c274154e122c0bb0925b8381d2dd51cad18264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960730"
---
# <span data-ttu-id="cd4af-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="cd4af-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="cd4af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd4af-102">SYNOPSIS</span></span>
<span data-ttu-id="cd4af-103">Ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="cd4af-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="cd4af-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd4af-104">SYNTAX</span></span>

### <span data-ttu-id="cd4af-105">Rozwinięty (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd4af-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd4af-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="cd4af-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd4af-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd4af-107">DESCRIPTION</span></span>
<span data-ttu-id="cd4af-108">Polecenie Set-AzKeyVaultCertificateIssuer ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="cd4af-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="cd4af-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd4af-109">EXAMPLES</span></span>

### <span data-ttu-id="cd4af-110">Przykład 1. Ustawianie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="cd4af-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetail -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="cd4af-111">To polecenie ustawia właściwości wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="cd4af-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="cd4af-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd4af-112">PARAMETERS</span></span>

### <span data-ttu-id="cd4af-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="cd4af-113">-AccountId</span></span>
<span data-ttu-id="cd4af-114">Określa identyfikator konta wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="cd4af-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="cd4af-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="cd4af-115">-ApiKey</span></span>
<span data-ttu-id="cd4af-116">Określa klucz interfejsu API wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="cd4af-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="cd4af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd4af-117">-DefaultProfile</span></span>
<span data-ttu-id="cd4af-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cd4af-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd4af-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd4af-119">-InputObject</span></span>
<span data-ttu-id="cd4af-120">Określa wystawcę certyfikatu do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="cd4af-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="cd4af-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="cd4af-121">-IssuerProvider</span></span>
<span data-ttu-id="cd4af-122">Określa typ wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="cd4af-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="cd4af-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cd4af-123">-Name</span></span>
<span data-ttu-id="cd4af-124">Określa nazwę wystawcy.</span><span class="sxs-lookup"><span data-stu-id="cd4af-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="cd4af-125">- OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="cd4af-125">-OrganizationDetails</span></span>
<span data-ttu-id="cd4af-126">Szczegóły organizacji, która ma zostać użyta wraz z wystawcą.</span><span class="sxs-lookup"><span data-stu-id="cd4af-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="cd4af-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd4af-127">-PassThru</span></span>
<span data-ttu-id="cd4af-128">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="cd4af-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cd4af-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cd4af-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd4af-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cd4af-130">-VaultName</span></span>
<span data-ttu-id="cd4af-131">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cd4af-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="cd4af-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd4af-132">-Confirm</span></span>
<span data-ttu-id="cd4af-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cd4af-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd4af-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd4af-134">-WhatIf</span></span>
<span data-ttu-id="cd4af-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd4af-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd4af-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cd4af-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd4af-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd4af-137">CommonParameters</span></span>
<span data-ttu-id="cd4af-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd4af-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd4af-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd4af-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd4af-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd4af-140">INPUTS</span></span>

### <span data-ttu-id="cd4af-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="cd4af-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="cd4af-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="cd4af-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="cd4af-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd4af-143">OUTPUTS</span></span>

### <span data-ttu-id="cd4af-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="cd4af-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="cd4af-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd4af-145">NOTES</span></span>

## <span data-ttu-id="cd4af-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd4af-146">RELATED LINKS</span></span>

[<span data-ttu-id="cd4af-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="cd4af-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="cd4af-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="cd4af-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

