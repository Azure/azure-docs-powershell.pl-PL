---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: c6d99fb2b6b568b090cb0ed86277b06fcde28115
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199994"
---
# <span data-ttu-id="f8e9b-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f8e9b-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="f8e9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e9b-103">Usuwa certyfikat z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="f8e9b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f8e9b-104">SYNTAX</span></span>

### <span data-ttu-id="f8e9b-105">ByVaultNameAndName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="f8e9b-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8e9b-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="f8e9b-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8e9b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f8e9b-107">DESCRIPTION</span></span>
<span data-ttu-id="f8e9b-108">Polecenie **cmdlet Remove-AzKeyVaultCertificate** usuwa certyfikat z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="f8e9b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f8e9b-109">EXAMPLES</span></span>

### <span data-ttu-id="f8e9b-110">Przykład 1. Usuwanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="f8e9b-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       4/11/2018 4:28:39 PM

                     [Not After]
                       10/11/2018 4:38:39 PM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contosokv01.vault.azure.net:443/keys/selfsigned01/968c3920884a435abf8faea11f565456
SecretId           : https://contosokv01.vault.azure.net:443/secrets/selfsigned01/968c3920884a435abf8faea11f565456
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Purgeable
ScheduledPurgeDate :
DeletedDate        :
Enabled            : True
Expires            : 10/11/2018 11:38:39 PM
NotBefore          : 4/11/2018 11:28:39 PM
Created            : 4/11/2018 11:38:39 PM
Updated            : 4/11/2018 11:38:39 PM
Tags               :
VaultName          : ContosoKV01
Name               : SelfSigned01
Version            : 968c3920884a435abf8faea11f565456
Id                 : https://contosokv01.vault.azure.net:443/certificates/selfsigned01/968c3920884a435abf8faea11f565456
```

<span data-ttu-id="f8e9b-111">To polecenie usuwa certyfikat o nazwie SelfSigned01 z magazynu kluczy o nazwie ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="f8e9b-112">To polecenie określa *parametr Force.*</span><span class="sxs-lookup"><span data-stu-id="f8e9b-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f8e9b-113">Dlatego polecenie cmdlet nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="f8e9b-114">Przykład 2. Trwałe czyszczenie usuniętego certyfikatu z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="f8e9b-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="f8e9b-115">To polecenie trwale usuwa certyfikat o nazwie "MyCert" z magazynu kluczy o nazwie "Contoso".</span><span class="sxs-lookup"><span data-stu-id="f8e9b-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="f8e9b-116">Wykonanie tego polecenia cmdlet wymaga uprawnienia "przeczyszczania", które musi być wcześniej i jawnie udzielone użytkownikowi w tym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="f8e9b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8e9b-117">PARAMETERS</span></span>

### <span data-ttu-id="f8e9b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e9b-118">-DefaultProfile</span></span>
<span data-ttu-id="f8e9b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f8e9b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8e9b-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f8e9b-120">-Force</span></span>
<span data-ttu-id="f8e9b-121">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f8e9b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8e9b-122">-InputObject</span></span>
<span data-ttu-id="f8e9b-123">Obiekt Certificate.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-123">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8e9b-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f8e9b-124">-InRemovedState</span></span>
<span data-ttu-id="f8e9b-125">Jeśli występuje, usuwa usunięty wcześniej certyfikat na stałe.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="f8e9b-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f8e9b-126">-Name</span></span>
<span data-ttu-id="f8e9b-127">Określa nazwę certyfikatu, który to polecenie cmdlet usuwa z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="f8e9b-128">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) certyfikatu na podstawie nazwy, która jest określana przez ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e9b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8e9b-129">-PassThru</span></span>
<span data-ttu-id="f8e9b-130">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f8e9b-131">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f8e9b-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f8e9b-132">-VaultName</span></span>
<span data-ttu-id="f8e9b-133">Określa nazwę magazynu kluczy, z którego to polecenie cmdlet usuwa certyfikat.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="f8e9b-134">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, która jest określana przez ten parametr i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e9b-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8e9b-135">-Confirm</span></span>
<span data-ttu-id="f8e9b-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e9b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8e9b-137">-WhatIf</span></span>
<span data-ttu-id="f8e9b-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8e9b-139">Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8e9b-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e9b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e9b-141">CommonParameters</span></span>
<span data-ttu-id="f8e9b-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8e9b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e9b-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8e9b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e9b-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8e9b-144">INPUTS</span></span>

### <span data-ttu-id="f8e9b-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f8e9b-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="f8e9b-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8e9b-146">OUTPUTS</span></span>

### <span data-ttu-id="f8e9b-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f8e9b-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="f8e9b-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f8e9b-148">NOTES</span></span>

## <span data-ttu-id="f8e9b-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8e9b-149">RELATED LINKS</span></span>

[<span data-ttu-id="f8e9b-150">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f8e9b-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="f8e9b-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f8e9b-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="f8e9b-152">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f8e9b-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="f8e9b-153">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="f8e9b-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
