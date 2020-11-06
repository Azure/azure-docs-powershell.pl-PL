---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: aee18adf3530976af4b17ffa15f94624248a7db7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545223"
---
# <span data-ttu-id="59144-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="59144-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="59144-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59144-102">SYNOPSIS</span></span>
<span data-ttu-id="59144-103">Umożliwia usunięcie kontaktu zarejestrowanego dla powiadomień o certyfikatach z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="59144-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59144-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59144-104">SYNTAX</span></span>

### <span data-ttu-id="59144-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="59144-105">ByName (Default)</span></span>
```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59144-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="59144-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59144-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="59144-107">ByResourceId</span></span>
```
Remove-AzureKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59144-108">Opis</span><span class="sxs-lookup"><span data-stu-id="59144-108">DESCRIPTION</span></span>
<span data-ttu-id="59144-109">Polecenie cmdlet **Remove-AzureKeyVaultCertificateContact** umożliwia usunięcie kontaktu zarejestrowanego dla powiadomień o certyfikatach z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="59144-109">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="59144-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59144-110">EXAMPLES</span></span>

### <span data-ttu-id="59144-111">Przykład 1: Usuwanie kontaktu z certyfikatem</span><span class="sxs-lookup"><span data-stu-id="59144-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="59144-112">To polecenie usuwa Patti w magazynie kluczy Contoso01 w pełni jako kontakt certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="59144-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="59144-113">Jeśli PassThru jest określony, polecenie cmdlet zwraca listę pozostałych kontaktów z certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="59144-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="59144-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59144-114">PARAMETERS</span></span>

### <span data-ttu-id="59144-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59144-115">-DefaultProfile</span></span>
<span data-ttu-id="59144-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="59144-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59144-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="59144-117">-EmailAddress</span></span>
<span data-ttu-id="59144-118">Określa adres e-mail kontaktu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="59144-118">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59144-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="59144-119">-InputObject</span></span>
<span data-ttu-id="59144-120">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="59144-120">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59144-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59144-121">-PassThru</span></span>
<span data-ttu-id="59144-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="59144-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="59144-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="59144-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59144-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59144-124">-ResourceId</span></span>
<span data-ttu-id="59144-125">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="59144-125">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59144-126">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="59144-126">-VaultName</span></span>
<span data-ttu-id="59144-127">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="59144-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59144-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59144-128">-Confirm</span></span>
<span data-ttu-id="59144-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59144-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59144-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59144-130">-WhatIf</span></span>
<span data-ttu-id="59144-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59144-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59144-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="59144-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59144-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59144-133">CommonParameters</span></span>
<span data-ttu-id="59144-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59144-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59144-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59144-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59144-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59144-136">INPUTS</span></span>

### <span data-ttu-id="59144-137">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="59144-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="59144-138">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="59144-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="59144-139">System. String</span><span class="sxs-lookup"><span data-stu-id="59144-139">System.String</span></span>

## <span data-ttu-id="59144-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59144-140">OUTPUTS</span></span>

### <span data-ttu-id="59144-141">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="59144-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="59144-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59144-142">NOTES</span></span>

## <span data-ttu-id="59144-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59144-143">RELATED LINKS</span></span>

[<span data-ttu-id="59144-144">Dodaj-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="59144-144">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="59144-145">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="59144-145">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

