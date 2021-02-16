---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 12fe8cdc0e8e7210a2db7c7c6ccab1a0fcceeba3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199987"
---
# <span data-ttu-id="3980e-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3980e-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="3980e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3980e-102">SYNOPSIS</span></span>
<span data-ttu-id="3980e-103">Usuwa kontakt zarejestrowany dla powiadomień o certyfikatach z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="3980e-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="3980e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3980e-104">SYNTAX</span></span>

### <span data-ttu-id="3980e-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="3980e-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3980e-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="3980e-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3980e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3980e-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3980e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3980e-108">DESCRIPTION</span></span>
<span data-ttu-id="3980e-109">Polecenie **cmdlet Remove-AzKeyVaultCertificateContact** usuwa kontakt zarejestrowany dla powiadomień o certyfikatach z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="3980e-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="3980e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3980e-110">EXAMPLES</span></span>

### <span data-ttu-id="3980e-111">Przykład 1. Usuwanie kontaktu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="3980e-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="3980e-112">To polecenie usuwa Patti Fuller jako kontakt certyfikatu dla magazynu kluczy Contoso01.</span><span class="sxs-lookup"><span data-stu-id="3980e-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="3980e-113">Jeśli zostanie określona wartość PassThru, polecenie cmdlet zwróci listę pozostałych kontaktów certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="3980e-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="3980e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3980e-114">PARAMETERS</span></span>

### <span data-ttu-id="3980e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3980e-115">-DefaultProfile</span></span>
<span data-ttu-id="3980e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3980e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3980e-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="3980e-117">-EmailAddress</span></span>
<span data-ttu-id="3980e-118">Określa adres e-mail kontaktu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="3980e-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="3980e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3980e-119">-InputObject</span></span>
<span data-ttu-id="3980e-120">Obiekt KeyVault.</span><span class="sxs-lookup"><span data-stu-id="3980e-120">KeyVault object.</span></span>

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

### <span data-ttu-id="3980e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3980e-121">-PassThru</span></span>
<span data-ttu-id="3980e-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3980e-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3980e-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3980e-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3980e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3980e-124">-ResourceId</span></span>
<span data-ttu-id="3980e-125">Identyfikator zasobu KeyVault.</span><span class="sxs-lookup"><span data-stu-id="3980e-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="3980e-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3980e-126">-VaultName</span></span>
<span data-ttu-id="3980e-127">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="3980e-127">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="3980e-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3980e-128">-Confirm</span></span>
<span data-ttu-id="3980e-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3980e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3980e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3980e-130">-WhatIf</span></span>
<span data-ttu-id="3980e-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3980e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3980e-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3980e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3980e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3980e-133">CommonParameters</span></span>
<span data-ttu-id="3980e-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3980e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3980e-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3980e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3980e-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3980e-136">INPUTS</span></span>

### <span data-ttu-id="3980e-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3980e-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="3980e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3980e-138">System.String</span></span>

## <span data-ttu-id="3980e-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3980e-139">OUTPUTS</span></span>

### <span data-ttu-id="3980e-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3980e-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="3980e-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3980e-141">NOTES</span></span>

## <span data-ttu-id="3980e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3980e-142">RELATED LINKS</span></span>

[<span data-ttu-id="3980e-143">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3980e-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="3980e-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3980e-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

