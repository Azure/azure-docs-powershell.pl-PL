---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 5757a9fb050d69cdf0ef0e648b0d446de1e3ee24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891242"
---
# <span data-ttu-id="97f8a-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="97f8a-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="97f8a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="97f8a-103">Odkrycie usuniętego certyfikatu w magazynie kluczy w stanie aktywnym.</span><span class="sxs-lookup"><span data-stu-id="97f8a-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="97f8a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97f8a-104">SYNTAX</span></span>

```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97f8a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="97f8a-105">DESCRIPTION</span></span>
<span data-ttu-id="97f8a-106">Polecenie cmdlet **Undo-AzKeyVaultCertificateRemoval** powoduje odzyskanie uprzednio usuniętego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="97f8a-106">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="97f8a-107">Odzyskany certyfikat będzie aktywny i może być wykorzystywany we wszystkich operacjach.</span><span class="sxs-lookup"><span data-stu-id="97f8a-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="97f8a-108">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="97f8a-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="97f8a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97f8a-109">EXAMPLES</span></span>

### <span data-ttu-id="97f8a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="97f8a-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="97f8a-111">To polecenie odzyska certyfikat, który został wcześniej usunięty, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="97f8a-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="97f8a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97f8a-112">PARAMETERS</span></span>

### <span data-ttu-id="97f8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f8a-113">-DefaultProfile</span></span>
<span data-ttu-id="97f8a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="97f8a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97f8a-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="97f8a-115">-Name</span></span>
<span data-ttu-id="97f8a-116">Nazwa certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="97f8a-116">Certificate name.</span></span>
<span data-ttu-id="97f8a-117">Polecenie cmdlet tworzy nazwę FQDN certyfikatu na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="97f8a-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f8a-118">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="97f8a-118">-VaultName</span></span>
<span data-ttu-id="97f8a-119">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="97f8a-119">Vault name.</span></span>
<span data-ttu-id="97f8a-120">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="97f8a-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="97f8a-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97f8a-121">-Confirm</span></span>
<span data-ttu-id="97f8a-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97f8a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97f8a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97f8a-123">-WhatIf</span></span>
<span data-ttu-id="97f8a-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97f8a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97f8a-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="97f8a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97f8a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f8a-126">CommonParameters</span></span>
<span data-ttu-id="97f8a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97f8a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f8a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97f8a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f8a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97f8a-129">INPUTS</span></span>

### <span data-ttu-id="97f8a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="97f8a-130">System.String</span></span>

## <span data-ttu-id="97f8a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97f8a-131">OUTPUTS</span></span>

### <span data-ttu-id="97f8a-132">Microsoft. Azure. Commands. platforming. models. Certificate.</span><span class="sxs-lookup"><span data-stu-id="97f8a-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="97f8a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97f8a-133">NOTES</span></span>

## <span data-ttu-id="97f8a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97f8a-134">RELATED LINKS</span></span>

[<span data-ttu-id="97f8a-135">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="97f8a-135">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="97f8a-136">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="97f8a-136">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
