---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 33024ce7002975848a98ff8bdfd6188196a96e6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718918"
---
# <span data-ttu-id="768f4-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="768f4-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="768f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="768f4-102">SYNOPSIS</span></span>
<span data-ttu-id="768f4-103">Odkrycie usuniętego certyfikatu w magazynie kluczy w stanie aktywnym.</span><span class="sxs-lookup"><span data-stu-id="768f4-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="768f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="768f4-104">SYNTAX</span></span>

### <span data-ttu-id="768f4-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="768f4-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="768f4-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="768f4-106">InputObject</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="768f4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="768f4-107">DESCRIPTION</span></span>
<span data-ttu-id="768f4-108">Polecenie cmdlet **Undo-AzureKeyVaultCertificateRemoval** powoduje odzyskanie uprzednio usuniętego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="768f4-108">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="768f4-109">Odzyskany certyfikat będzie aktywny i może być wykorzystywany we wszystkich operacjach.</span><span class="sxs-lookup"><span data-stu-id="768f4-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="768f4-110">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="768f4-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="768f4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="768f4-111">EXAMPLES</span></span>

### <span data-ttu-id="768f4-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="768f4-112">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="768f4-113">To polecenie odzyska certyfikat, który został wcześniej usunięty, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="768f4-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="768f4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="768f4-114">PARAMETERS</span></span>

### <span data-ttu-id="768f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="768f4-115">-DefaultProfile</span></span>
<span data-ttu-id="768f4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="768f4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="768f4-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="768f4-117">-InputObject</span></span>
<span data-ttu-id="768f4-118">Usunięto obiekt certyfikatu</span><span class="sxs-lookup"><span data-stu-id="768f4-118">Deleted Certificate object</span></span>

```yaml
Type: PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="768f4-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="768f4-119">-Name</span></span>
<span data-ttu-id="768f4-120">Nazwa certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="768f4-120">Certificate name.</span></span>
<span data-ttu-id="768f4-121">Polecenie cmdlet tworzy nazwę FQDN certyfikatu na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="768f4-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="768f4-122">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="768f4-122">-VaultName</span></span>
<span data-ttu-id="768f4-123">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="768f4-123">Vault name.</span></span>
<span data-ttu-id="768f4-124">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="768f4-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="768f4-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="768f4-125">-Confirm</span></span>
<span data-ttu-id="768f4-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="768f4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="768f4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="768f4-127">-WhatIf</span></span>
<span data-ttu-id="768f4-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="768f4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="768f4-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="768f4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="768f4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="768f4-130">CommonParameters</span></span>
<span data-ttu-id="768f4-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="768f4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="768f4-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="768f4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="768f4-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="768f4-133">INPUTS</span></span>

### <span data-ttu-id="768f4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="768f4-134">System.String</span></span>

## <span data-ttu-id="768f4-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="768f4-135">OUTPUTS</span></span>

### <span data-ttu-id="768f4-136">Microsoft. Azure. Commands. platforming. models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="768f4-136">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="768f4-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="768f4-137">NOTES</span></span>

## <span data-ttu-id="768f4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="768f4-138">RELATED LINKS</span></span>

[<span data-ttu-id="768f4-139">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="768f4-139">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="768f4-140">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="768f4-140">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
