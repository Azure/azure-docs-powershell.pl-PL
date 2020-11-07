---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 8498ea769f8f9a3f7107cb7dd883e79633b9aff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717076"
---
# <span data-ttu-id="7c16d-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7c16d-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="7c16d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c16d-102">SYNOPSIS</span></span>
<span data-ttu-id="7c16d-103">Usuwa certyfikat z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="7c16d-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c16d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c16d-104">SYNTAX</span></span>

### <span data-ttu-id="7c16d-105">ByVaultNameAndName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7c16d-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c16d-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="7c16d-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c16d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7c16d-107">DESCRIPTION</span></span>
<span data-ttu-id="7c16d-108">Polecenie cmdlet **Remove-AzureKeyVaultCertificate** usuwa certyfikat z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="7c16d-108">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="7c16d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c16d-109">EXAMPLES</span></span>

### <span data-ttu-id="7c16d-110">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="7c16d-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

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

<span data-ttu-id="7c16d-111">To polecenie usuwa certyfikat o nazwie SelfSigned01 z magazynu kluczy o nazwie ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="7c16d-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="7c16d-112">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="7c16d-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7c16d-113">Dlatego polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7c16d-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="7c16d-114">Przykład 2: trwałe przeczyszczanie usuniętego certyfikatu z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="7c16d-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="7c16d-115">To polecenie powoduje trwałe usunięcie certyfikatu o nazwie "Moje CERT" z magazynu kluczy o nazwie "contoso".</span><span class="sxs-lookup"><span data-stu-id="7c16d-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="7c16d-116">Wykonanie tego polecenia cmdlet wymaga uprawnienia "Wyczyść", które musi być wcześniej i wyraźnie udzielone użytkownikowi w tym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="7c16d-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="7c16d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c16d-117">PARAMETERS</span></span>

### <span data-ttu-id="7c16d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c16d-118">-DefaultProfile</span></span>
<span data-ttu-id="7c16d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7c16d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c16d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7c16d-120">-Force</span></span>
<span data-ttu-id="7c16d-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7c16d-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c16d-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7c16d-122">-InputObject</span></span>
<span data-ttu-id="7c16d-123">Obiekt Certificate (certyfikat).</span><span class="sxs-lookup"><span data-stu-id="7c16d-123">Certificate Object.</span></span>

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

### <span data-ttu-id="7c16d-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="7c16d-124">-InRemovedState</span></span>
<span data-ttu-id="7c16d-125">Jeśli ta operacja jest obecna, usuwa już trwale usunięty certyfikat</span><span class="sxs-lookup"><span data-stu-id="7c16d-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="7c16d-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7c16d-126">-Name</span></span>
<span data-ttu-id="7c16d-127">Określa nazwę certyfikatu usuniętego przez ten aplet polecenia z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="7c16d-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="7c16d-128">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) certyfikatu na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="7c16d-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="7c16d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c16d-129">-PassThru</span></span>
<span data-ttu-id="7c16d-130">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="7c16d-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7c16d-131">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7c16d-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7c16d-132">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="7c16d-132">-VaultName</span></span>
<span data-ttu-id="7c16d-133">Określa nazwę magazynu kluczy, z którego to polecenie cmdlet usuwa certyfikat.</span><span class="sxs-lookup"><span data-stu-id="7c16d-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="7c16d-134">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="7c16d-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="7c16d-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7c16d-135">-Confirm</span></span>
<span data-ttu-id="7c16d-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c16d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c16d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c16d-137">-WhatIf</span></span>
<span data-ttu-id="7c16d-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c16d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c16d-139">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c16d-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c16d-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7c16d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c16d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c16d-141">CommonParameters</span></span>
<span data-ttu-id="7c16d-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c16d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c16d-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c16d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c16d-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c16d-144">INPUTS</span></span>

### <span data-ttu-id="7c16d-145">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7c16d-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="7c16d-146">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7c16d-146">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7c16d-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c16d-147">OUTPUTS</span></span>

### <span data-ttu-id="7c16d-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7c16d-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="7c16d-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c16d-149">NOTES</span></span>

## <span data-ttu-id="7c16d-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c16d-150">RELATED LINKS</span></span>

[<span data-ttu-id="7c16d-151">Dodaj-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7c16d-151">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="7c16d-152">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7c16d-152">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="7c16d-153">Import — AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7c16d-153">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="7c16d-154">Cofanie — AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="7c16d-154">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)