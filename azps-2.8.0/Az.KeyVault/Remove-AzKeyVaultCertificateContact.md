---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 0f1768bec11c5a85e97cdb27e6e9a3195c3880b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705138"
---
# <span data-ttu-id="f8d96-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="f8d96-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="f8d96-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8d96-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d96-103">Umożliwia usunięcie kontaktu zarejestrowanego dla powiadomień o certyfikatach z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f8d96-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="f8d96-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8d96-104">SYNTAX</span></span>

### <span data-ttu-id="f8d96-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f8d96-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d96-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="f8d96-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d96-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f8d96-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8d96-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f8d96-108">DESCRIPTION</span></span>
<span data-ttu-id="f8d96-109">Polecenie cmdlet **Remove-AzKeyVaultCertificateContact** umożliwia usunięcie kontaktu zarejestrowanego dla powiadomień o certyfikatach z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f8d96-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="f8d96-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8d96-110">EXAMPLES</span></span>

### <span data-ttu-id="f8d96-111">Przykład 1: Usuwanie kontaktu z certyfikatem</span><span class="sxs-lookup"><span data-stu-id="f8d96-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="f8d96-112">To polecenie usuwa Patti w magazynie kluczy Contoso01 w pełni jako kontakt certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f8d96-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="f8d96-113">Jeśli PassThru jest określony, polecenie cmdlet zwraca listę pozostałych kontaktów z certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="f8d96-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="f8d96-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8d96-114">PARAMETERS</span></span>

### <span data-ttu-id="f8d96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d96-115">-DefaultProfile</span></span>
<span data-ttu-id="f8d96-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f8d96-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8d96-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="f8d96-117">-EmailAddress</span></span>
<span data-ttu-id="f8d96-118">Określa adres e-mail kontaktu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="f8d96-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="f8d96-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f8d96-119">-InputObject</span></span>
<span data-ttu-id="f8d96-120">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="f8d96-120">KeyVault object.</span></span>

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

### <span data-ttu-id="f8d96-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8d96-121">-PassThru</span></span>
<span data-ttu-id="f8d96-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f8d96-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f8d96-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f8d96-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f8d96-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8d96-124">-ResourceId</span></span>
<span data-ttu-id="f8d96-125">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="f8d96-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="f8d96-126">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="f8d96-126">-VaultName</span></span>
<span data-ttu-id="f8d96-127">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f8d96-127">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="f8d96-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8d96-128">-Confirm</span></span>
<span data-ttu-id="f8d96-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8d96-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8d96-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8d96-130">-WhatIf</span></span>
<span data-ttu-id="f8d96-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8d96-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8d96-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f8d96-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8d96-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d96-133">CommonParameters</span></span>
<span data-ttu-id="f8d96-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8d96-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d96-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8d96-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d96-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8d96-136">INPUTS</span></span>

### <span data-ttu-id="f8d96-137">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f8d96-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="f8d96-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f8d96-138">System.String</span></span>

## <span data-ttu-id="f8d96-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8d96-139">OUTPUTS</span></span>

### <span data-ttu-id="f8d96-140">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="f8d96-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="f8d96-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8d96-141">NOTES</span></span>

## <span data-ttu-id="f8d96-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8d96-142">RELATED LINKS</span></span>

[<span data-ttu-id="f8d96-143">Dodaj-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="f8d96-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="f8d96-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="f8d96-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

