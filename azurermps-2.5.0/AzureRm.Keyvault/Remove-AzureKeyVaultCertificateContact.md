---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: 9bfb62388ce4a7a8994f4a618a4c1a00ac5868d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897390"
---
# <span data-ttu-id="1daa0-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1daa0-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="1daa0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1daa0-102">SYNOPSIS</span></span>
<span data-ttu-id="1daa0-103">Umożliwia usunięcie kontaktu zarejestrowanego dla powiadomień o certyfikatach z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1daa0-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1daa0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1daa0-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1daa0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1daa0-105">DESCRIPTION</span></span>
<span data-ttu-id="1daa0-106">Polecenie cmdlet **Remove-AzureKeyVaultCertificateContact** umożliwia usunięcie kontaktu zarejestrowanego dla powiadomień o certyfikatach z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1daa0-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="1daa0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1daa0-107">EXAMPLES</span></span>

### <span data-ttu-id="1daa0-108">Przykład 1: Usuwanie kontaktu z certyfikatem</span><span class="sxs-lookup"><span data-stu-id="1daa0-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="1daa0-109">To polecenie usuwa Patti w magazynie kluczy Contoso01 w pełni jako kontakt certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1daa0-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="1daa0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1daa0-110">PARAMETERS</span></span>

### <span data-ttu-id="1daa0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1daa0-111">-DefaultProfile</span></span>
<span data-ttu-id="1daa0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1daa0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1daa0-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="1daa0-113">-EmailAddress</span></span>
<span data-ttu-id="1daa0-114">Określa adres e-mail kontaktu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="1daa0-114">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1daa0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1daa0-115">-PassThru</span></span>
<span data-ttu-id="1daa0-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="1daa0-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1daa0-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1daa0-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1daa0-118">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="1daa0-118">-VaultName</span></span>
<span data-ttu-id="1daa0-119">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1daa0-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="1daa0-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1daa0-120">-Confirm</span></span>
<span data-ttu-id="1daa0-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1daa0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1daa0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1daa0-122">-WhatIf</span></span>
<span data-ttu-id="1daa0-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1daa0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1daa0-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1daa0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1daa0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1daa0-125">CommonParameters</span></span>
<span data-ttu-id="1daa0-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1daa0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1daa0-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1daa0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1daa0-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1daa0-128">INPUTS</span></span>

## <span data-ttu-id="1daa0-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1daa0-129">OUTPUTS</span></span>

### <span data-ttu-id="1daa0-130">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. platforming. modele. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="1daa0-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="1daa0-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1daa0-131">NOTES</span></span>

## <span data-ttu-id="1daa0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1daa0-132">RELATED LINKS</span></span>

[<span data-ttu-id="1daa0-133">Dodaj-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1daa0-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="1daa0-134">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1daa0-134">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

