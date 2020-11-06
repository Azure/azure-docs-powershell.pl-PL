---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: c91aa7e43a36e1218f304c3675f1d3c9635002c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551716"
---
# <span data-ttu-id="c8419-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c8419-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="c8419-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8419-102">SYNOPSIS</span></span>
<span data-ttu-id="c8419-103">Umożliwia usunięcie kontaktu zarejestrowanego dla powiadomień o certyfikatach z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="c8419-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8419-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8419-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8419-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8419-105">DESCRIPTION</span></span>
<span data-ttu-id="c8419-106">Polecenie cmdlet **Remove-AzureKeyVaultCertificateContact** umożliwia usunięcie kontaktu zarejestrowanego dla powiadomień o certyfikatach z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="c8419-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="c8419-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8419-107">EXAMPLES</span></span>

### <span data-ttu-id="c8419-108">Przykład 1: Usuwanie kontaktu z certyfikatem</span><span class="sxs-lookup"><span data-stu-id="c8419-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="c8419-109">To polecenie usuwa Patti w magazynie kluczy Contoso01 w pełni jako kontakt certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="c8419-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="c8419-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8419-110">PARAMETERS</span></span>

### <span data-ttu-id="c8419-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8419-111">-DefaultProfile</span></span>
<span data-ttu-id="c8419-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c8419-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8419-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="c8419-113">-EmailAddress</span></span>
<span data-ttu-id="c8419-114">Określa adres e-mail kontaktu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="c8419-114">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8419-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8419-115">-PassThru</span></span>
<span data-ttu-id="c8419-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c8419-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c8419-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c8419-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c8419-118">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="c8419-118">-VaultName</span></span>
<span data-ttu-id="c8419-119">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="c8419-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="c8419-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8419-120">-Confirm</span></span>
<span data-ttu-id="c8419-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8419-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8419-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8419-122">-WhatIf</span></span>
<span data-ttu-id="c8419-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8419-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8419-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c8419-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8419-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8419-125">CommonParameters</span></span>
<span data-ttu-id="c8419-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8419-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8419-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8419-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8419-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8419-128">INPUTS</span></span>

### <span data-ttu-id="c8419-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c8419-129">None</span></span>
<span data-ttu-id="c8419-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c8419-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8419-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8419-131">OUTPUTS</span></span>

### <span data-ttu-id="c8419-132">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. platforming. modele. PSKeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="c8419-132">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact]</span></span>

## <span data-ttu-id="c8419-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8419-133">NOTES</span></span>

## <span data-ttu-id="c8419-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8419-134">RELATED LINKS</span></span>

[<span data-ttu-id="c8419-135">Dodaj-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c8419-135">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="c8419-136">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c8419-136">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

