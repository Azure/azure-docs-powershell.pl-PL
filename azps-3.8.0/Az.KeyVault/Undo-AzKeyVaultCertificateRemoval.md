---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 7e9af7cd775726fc57b78f3fdead20f36dca13cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895205"
---
# <span data-ttu-id="68e75-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="68e75-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="68e75-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68e75-102">SYNOPSIS</span></span>
<span data-ttu-id="68e75-103">Odkrycie usuniętego certyfikatu w magazynie kluczy w stanie aktywnym.</span><span class="sxs-lookup"><span data-stu-id="68e75-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="68e75-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68e75-104">SYNTAX</span></span>

### <span data-ttu-id="68e75-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="68e75-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68e75-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="68e75-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68e75-107">Opis</span><span class="sxs-lookup"><span data-stu-id="68e75-107">DESCRIPTION</span></span>
<span data-ttu-id="68e75-108">Polecenie cmdlet **Undo-AzKeyVaultCertificateRemoval** powoduje odzyskanie uprzednio usuniętego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="68e75-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="68e75-109">Odzyskany certyfikat będzie aktywny i może być wykorzystywany we wszystkich operacjach.</span><span class="sxs-lookup"><span data-stu-id="68e75-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="68e75-110">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="68e75-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="68e75-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68e75-111">EXAMPLES</span></span>

### <span data-ttu-id="68e75-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="68e75-112">Example 1</span></span>
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

<span data-ttu-id="68e75-113">To polecenie odzyska certyfikat, który został wcześniej usunięty, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="68e75-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="68e75-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68e75-114">PARAMETERS</span></span>

### <span data-ttu-id="68e75-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e75-115">-DefaultProfile</span></span>
<span data-ttu-id="68e75-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="68e75-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68e75-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="68e75-117">-InputObject</span></span>
<span data-ttu-id="68e75-118">Usunięto obiekt certyfikatu</span><span class="sxs-lookup"><span data-stu-id="68e75-118">Deleted Certificate object</span></span>

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

### <span data-ttu-id="68e75-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68e75-119">-Name</span></span>
<span data-ttu-id="68e75-120">Nazwa certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="68e75-120">Certificate name.</span></span>
<span data-ttu-id="68e75-121">Polecenie cmdlet tworzy nazwę FQDN certyfikatu na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="68e75-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="68e75-122">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="68e75-122">-VaultName</span></span>
<span data-ttu-id="68e75-123">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="68e75-123">Vault name.</span></span>
<span data-ttu-id="68e75-124">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="68e75-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="68e75-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68e75-125">-Confirm</span></span>
<span data-ttu-id="68e75-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68e75-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68e75-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68e75-127">-WhatIf</span></span>
<span data-ttu-id="68e75-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68e75-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68e75-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68e75-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68e75-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e75-130">CommonParameters</span></span>
<span data-ttu-id="68e75-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68e75-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e75-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68e75-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e75-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68e75-133">INPUTS</span></span>

### <span data-ttu-id="68e75-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="68e75-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="68e75-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68e75-135">OUTPUTS</span></span>

### <span data-ttu-id="68e75-136">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="68e75-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="68e75-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68e75-137">NOTES</span></span>

## <span data-ttu-id="68e75-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68e75-138">RELATED LINKS</span></span>

[<span data-ttu-id="68e75-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="68e75-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="68e75-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="68e75-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
