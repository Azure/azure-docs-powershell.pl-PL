---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 375cc5493bd3b3cac31f4318df57e155eda918c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893069"
---
# <span data-ttu-id="8c373-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8c373-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="8c373-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c373-102">SYNOPSIS</span></span>
<span data-ttu-id="8c373-103">Umożliwia dodanie kontaktu do powiadomień o certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="8c373-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="8c373-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c373-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c373-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8c373-105">DESCRIPTION</span></span>
<span data-ttu-id="8c373-106">Polecenie cmdlet **Add-AzKeyVaultCertificateContact** umożliwia dodanie kontaktu dla magazynu kluczy na potrzeby powiadomień o certyfikatach w magazynie kluczy Azure.</span><span class="sxs-lookup"><span data-stu-id="8c373-106">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="8c373-107">Kontakt będzie otrzymywać aktualizacje dotyczące zdarzeń, takich jak certyfikat bliski wygaśnięcia, odnowienia certyfikatu itd.</span><span class="sxs-lookup"><span data-stu-id="8c373-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="8c373-108">Te zdarzenia są określone przez zasady certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8c373-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="8c373-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c373-109">EXAMPLES</span></span>

### <span data-ttu-id="8c373-110">Przykład 1: Dodawanie kontaktu z certyfikatem magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="8c373-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="8c373-111">To polecenie dodaje Patti jako kontakt certyfikatu dla magazynu kluczy ContosoKV01 i zwraca obiekt **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="8c373-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="8c373-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c373-112">PARAMETERS</span></span>

### <span data-ttu-id="8c373-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c373-113">-DefaultProfile</span></span>
<span data-ttu-id="8c373-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8c373-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c373-115">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8c373-115">-EmailAddress</span></span>
<span data-ttu-id="8c373-116">Określa adres e-mail kontaktu.</span><span class="sxs-lookup"><span data-stu-id="8c373-116">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="8c373-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c373-117">-PassThru</span></span>
<span data-ttu-id="8c373-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="8c373-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8c373-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8c373-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c373-120">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="8c373-120">-VaultName</span></span>
<span data-ttu-id="8c373-121">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="8c373-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="8c373-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c373-122">-Confirm</span></span>
<span data-ttu-id="8c373-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c373-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c373-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c373-124">-WhatIf</span></span>
<span data-ttu-id="8c373-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c373-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c373-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8c373-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c373-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c373-127">CommonParameters</span></span>
<span data-ttu-id="8c373-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c373-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c373-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c373-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c373-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c373-130">INPUTS</span></span>

### <span data-ttu-id="8c373-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8c373-131">None</span></span>
<span data-ttu-id="8c373-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8c373-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c373-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c373-133">OUTPUTS</span></span>

### <span data-ttu-id="8c373-134">Lista<Microsoft. Azure. Commands.. models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="8c373-134">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="8c373-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c373-135">NOTES</span></span>

## <span data-ttu-id="8c373-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c373-136">RELATED LINKS</span></span>

[<span data-ttu-id="8c373-137">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8c373-137">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="8c373-138">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8c373-138">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

