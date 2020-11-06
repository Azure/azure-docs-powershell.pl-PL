---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: af66ad82d37c29d1dcd455cb3ccf7ae11676828c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553272"
---
# <span data-ttu-id="42c88-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="42c88-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="42c88-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42c88-102">SYNOPSIS</span></span>
<span data-ttu-id="42c88-103">Umożliwia dodanie kontaktu do powiadomień o certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="42c88-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42c88-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42c88-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42c88-105">Opis</span><span class="sxs-lookup"><span data-stu-id="42c88-105">DESCRIPTION</span></span>
<span data-ttu-id="42c88-106">Polecenie cmdlet **Add-AzureKeyVaultCertificateContact** umożliwia dodanie kontaktu dla magazynu kluczy na potrzeby powiadomień o certyfikatach w magazynie kluczy Azure.</span><span class="sxs-lookup"><span data-stu-id="42c88-106">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="42c88-107">Kontakt będzie otrzymywać aktualizacje dotyczące zdarzeń, takich jak certyfikat bliski wygaśnięcia, odnowienia certyfikatu itd.</span><span class="sxs-lookup"><span data-stu-id="42c88-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="42c88-108">Te zdarzenia są określone przez zasady certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="42c88-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="42c88-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42c88-109">EXAMPLES</span></span>

### <span data-ttu-id="42c88-110">Przykład 1: Dodawanie kontaktu z certyfikatem magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="42c88-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="42c88-111">To polecenie dodaje Patti jako kontakt certyfikatu dla magazynu kluczy ContosoKV01 i zwraca obiekt **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="42c88-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="42c88-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42c88-112">PARAMETERS</span></span>

### <span data-ttu-id="42c88-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="42c88-113">-EmailAddress</span></span>
<span data-ttu-id="42c88-114">Określa adres e-mail kontaktu.</span><span class="sxs-lookup"><span data-stu-id="42c88-114">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42c88-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42c88-115">-PassThru</span></span>
<span data-ttu-id="42c88-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="42c88-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="42c88-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="42c88-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42c88-118">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="42c88-118">-VaultName</span></span>
<span data-ttu-id="42c88-119">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="42c88-119">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42c88-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42c88-120">-Confirm</span></span>
<span data-ttu-id="42c88-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42c88-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42c88-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42c88-122">-WhatIf</span></span>
<span data-ttu-id="42c88-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42c88-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42c88-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42c88-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42c88-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c88-125">-DefaultProfile</span></span>
<span data-ttu-id="42c88-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42c88-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42c88-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c88-127">CommonParameters</span></span>
<span data-ttu-id="42c88-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42c88-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c88-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42c88-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c88-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42c88-130">INPUTS</span></span>

## <span data-ttu-id="42c88-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42c88-131">OUTPUTS</span></span>

### <span data-ttu-id="42c88-132">Lista<Microsoft. Azure. Commands.. models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="42c88-132">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="42c88-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42c88-133">NOTES</span></span>

## <span data-ttu-id="42c88-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42c88-134">RELATED LINKS</span></span>

[<span data-ttu-id="42c88-135">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="42c88-135">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="42c88-136">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="42c88-136">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

