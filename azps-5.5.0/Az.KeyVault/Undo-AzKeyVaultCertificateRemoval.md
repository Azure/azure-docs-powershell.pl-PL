---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 7e9af7cd775726fc57b78f3fdead20f36dca13cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185458"
---
# <span data-ttu-id="a2068-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="a2068-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="a2068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2068-102">SYNOPSIS</span></span>
<span data-ttu-id="a2068-103">Przywraca usunięty certyfikat z magazynu kluczy do stanu aktywnego.</span><span class="sxs-lookup"><span data-stu-id="a2068-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="a2068-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a2068-104">SYNTAX</span></span>

### <span data-ttu-id="a2068-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a2068-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2068-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a2068-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2068-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a2068-107">DESCRIPTION</span></span>
<span data-ttu-id="a2068-108">Polecenie **cmdlet Undo-AzKeyVaultCertificateRemoval** spowoduje odzyskanie usuniętego wcześniej certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a2068-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="a2068-109">Odzyskany certyfikat będzie aktywny i będzie można go używać we wszystkich operacjach.</span><span class="sxs-lookup"><span data-stu-id="a2068-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="a2068-110">Aby wykonać tę operację, dzwoniący musi mieć uprawnienie do odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a2068-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="a2068-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a2068-111">EXAMPLES</span></span>

### <span data-ttu-id="a2068-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a2068-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/24/2018 10:58:13 AM

                [Not After]
                  11/24/2018 10:08:13 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/mycertificate/7fe415d5518240c1a6fce89986b8d334
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/mycertificate/7fe415d5518240c1a6fce89986b8d334
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Recoverable+Purgeable
Enabled       : True
Expires       : 11/24/2018 6:08:13 PM
NotBefore     : 5/24/2018 5:58:13 PM
Created       : 5/24/2018 6:08:13 PM
Updated       : 5/24/2018 6:08:13 PM
Tags          :
VaultName     : MyKeyVault
Name          : MyCertificate
Version       : 7fe415d5518240c1a6fce89986b8d334
Id            : https://mykeyvault.vault.azure.net:443/certificates/mycertificate/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="a2068-113">To polecenie spowoduje odzyskanie wcześniej usuniętego certyfikatu w stanie aktywnym i użytecznym.</span><span class="sxs-lookup"><span data-stu-id="a2068-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="a2068-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2068-114">PARAMETERS</span></span>

### <span data-ttu-id="a2068-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2068-115">-DefaultProfile</span></span>
<span data-ttu-id="a2068-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a2068-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2068-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2068-117">-InputObject</span></span>
<span data-ttu-id="a2068-118">Usunięty obiekt Certyfikat</span><span class="sxs-lookup"><span data-stu-id="a2068-118">Deleted Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2068-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a2068-119">-Name</span></span>
<span data-ttu-id="a2068-120">Nazwa certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a2068-120">Certificate name.</span></span>
<span data-ttu-id="a2068-121">Polecenie cmdlet konstruuje nazwę FQDN certyfikatu z nazwy magazynu, obecnie wybranego środowiska i nazwy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a2068-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2068-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a2068-122">-VaultName</span></span>
<span data-ttu-id="a2068-123">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="a2068-123">Vault name.</span></span>
<span data-ttu-id="a2068-124">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="a2068-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2068-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a2068-125">-Confirm</span></span>
<span data-ttu-id="a2068-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a2068-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2068-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2068-127">-WhatIf</span></span>
<span data-ttu-id="a2068-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2068-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2068-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a2068-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2068-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2068-130">CommonParameters</span></span>
<span data-ttu-id="a2068-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2068-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2068-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2068-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2068-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2068-133">INPUTS</span></span>

### <span data-ttu-id="a2068-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a2068-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="a2068-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2068-135">OUTPUTS</span></span>

### <span data-ttu-id="a2068-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a2068-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="a2068-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a2068-137">NOTES</span></span>

## <span data-ttu-id="a2068-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2068-138">RELATED LINKS</span></span>

[<span data-ttu-id="a2068-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a2068-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="a2068-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a2068-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
