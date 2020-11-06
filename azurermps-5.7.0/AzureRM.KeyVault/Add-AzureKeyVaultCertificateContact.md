---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 96f793c763a3e9a710c7e401c29880ccc0136b38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552900"
---
# <span data-ttu-id="03995-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="03995-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="03995-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03995-102">SYNOPSIS</span></span>
<span data-ttu-id="03995-103">Umożliwia dodanie kontaktu do powiadomień o certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="03995-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03995-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03995-104">SYNTAX</span></span>

### <span data-ttu-id="03995-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="03995-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03995-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="03995-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03995-107">Opis</span><span class="sxs-lookup"><span data-stu-id="03995-107">DESCRIPTION</span></span>
<span data-ttu-id="03995-108">Polecenie cmdlet **Add-AzureKeyVaultCertificateContact** umożliwia dodanie kontaktu dla magazynu kluczy na potrzeby powiadomień o certyfikatach w magazynie kluczy Azure.</span><span class="sxs-lookup"><span data-stu-id="03995-108">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="03995-109">Kontakt będzie otrzymywać aktualizacje dotyczące zdarzeń, takich jak certyfikat bliski wygaśnięcia, odnowienia certyfikatu itd.</span><span class="sxs-lookup"><span data-stu-id="03995-109">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="03995-110">Te zdarzenia są określone przez zasady certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="03995-110">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="03995-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03995-111">EXAMPLES</span></span>

### <span data-ttu-id="03995-112">Przykład 1: Dodawanie kontaktu z certyfikatem magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="03995-112">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="03995-113">To polecenie dodaje Patti jako kontakt certyfikatu dla magazynu kluczy ContosoKV01 i zwraca obiekt **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="03995-113">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="03995-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03995-114">PARAMETERS</span></span>

### <span data-ttu-id="03995-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03995-115">-DefaultProfile</span></span>
<span data-ttu-id="03995-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="03995-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03995-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="03995-117">-EmailAddress</span></span>
<span data-ttu-id="03995-118">Określa adres e-mail kontaktu.</span><span class="sxs-lookup"><span data-stu-id="03995-118">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="03995-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03995-119">-InputObject</span></span>
<span data-ttu-id="03995-120">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="03995-120">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03995-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03995-121">-PassThru</span></span>
<span data-ttu-id="03995-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="03995-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03995-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="03995-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03995-124">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="03995-124">-VaultName</span></span>
<span data-ttu-id="03995-125">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="03995-125">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03995-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03995-126">-Confirm</span></span>
<span data-ttu-id="03995-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03995-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03995-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03995-128">-WhatIf</span></span>
<span data-ttu-id="03995-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03995-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03995-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03995-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03995-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03995-131">CommonParameters</span></span>
<span data-ttu-id="03995-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03995-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03995-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03995-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03995-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03995-134">INPUTS</span></span>

### <span data-ttu-id="03995-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="03995-135">None</span></span>
<span data-ttu-id="03995-136">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="03995-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03995-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03995-137">OUTPUTS</span></span>

### <span data-ttu-id="03995-138">Lista<Microsoft. Azure. Commands.. models. PSKeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="03995-138">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="03995-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03995-139">NOTES</span></span>

## <span data-ttu-id="03995-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03995-140">RELATED LINKS</span></span>

[<span data-ttu-id="03995-141">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="03995-141">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="03995-142">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="03995-142">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

