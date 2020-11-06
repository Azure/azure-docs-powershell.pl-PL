---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 91fee65a201de8babc7ef7aa09973f1e98f95cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553243"
---
# <span data-ttu-id="bbb72-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="bbb72-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="bbb72-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bbb72-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb72-103">Odkrycie usuniętego certyfikatu w magazynie kluczy w stanie aktywnym.</span><span class="sxs-lookup"><span data-stu-id="bbb72-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbb72-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bbb72-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbb72-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bbb72-105">DESCRIPTION</span></span>
<span data-ttu-id="bbb72-106">Polecenie cmdlet **Undo-AzureKeyVaultCertificateRemoval** powoduje odzyskanie uprzednio usuniętego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="bbb72-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="bbb72-107">Odzyskany certyfikat będzie aktywny i może być wykorzystywany we wszystkich operacjach.</span><span class="sxs-lookup"><span data-stu-id="bbb72-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="bbb72-108">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="bbb72-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="bbb72-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bbb72-109">EXAMPLES</span></span>

### <span data-ttu-id="bbb72-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bbb72-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="bbb72-111">To polecenie odzyska certyfikat, który został wcześniej usunięty, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="bbb72-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="bbb72-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bbb72-112">PARAMETERS</span></span>

### <span data-ttu-id="bbb72-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bbb72-113">-Name</span></span>
<span data-ttu-id="bbb72-114">Nazwa certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="bbb72-114">Certificate name.</span></span>
<span data-ttu-id="bbb72-115">Polecenie cmdlet tworzy nazwę FQDN certyfikatu na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="bbb72-115">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb72-116">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="bbb72-116">-VaultName</span></span>
<span data-ttu-id="bbb72-117">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="bbb72-117">Vault name.</span></span>
<span data-ttu-id="bbb72-118">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="bbb72-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb72-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bbb72-119">-Confirm</span></span>
<span data-ttu-id="bbb72-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbb72-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbb72-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbb72-121">-WhatIf</span></span>
<span data-ttu-id="bbb72-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbb72-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbb72-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bbb72-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbb72-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb72-124">-DefaultProfile</span></span>
<span data-ttu-id="bbb72-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbb72-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbb72-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb72-126">CommonParameters</span></span>
<span data-ttu-id="bbb72-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbb72-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb72-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbb72-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb72-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbb72-129">INPUTS</span></span>

### <span data-ttu-id="bbb72-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bbb72-130">System.String</span></span>

## <span data-ttu-id="bbb72-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bbb72-131">OUTPUTS</span></span>

### <span data-ttu-id="bbb72-132">Microsoft. Azure. Commands. platforming. models. Certificate.</span><span class="sxs-lookup"><span data-stu-id="bbb72-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="bbb72-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bbb72-133">NOTES</span></span>

## <span data-ttu-id="bbb72-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbb72-134">RELATED LINKS</span></span>

[<span data-ttu-id="bbb72-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="bbb72-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="bbb72-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="bbb72-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
