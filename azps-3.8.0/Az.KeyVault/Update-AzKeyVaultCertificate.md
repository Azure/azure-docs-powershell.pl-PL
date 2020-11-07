---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
ms.openlocfilehash: 8c4bb4813c2d07577d80743906a4f8155bc81282
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895170"
---
# <span data-ttu-id="0f349-101">Update-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0f349-101">Update-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="0f349-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f349-102">SYNOPSIS</span></span>
<span data-ttu-id="0f349-103">Modyfikowanie atrybutów edytowalnych certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0f349-103">Modifies editable attributes of a certificate.</span></span>

## <span data-ttu-id="0f349-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f349-104">SYNTAX</span></span>

### <span data-ttu-id="0f349-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0f349-105">ByName (Default)</span></span>
```
Update-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f349-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f349-106">ByInputObject</span></span>
```
Update-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f349-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0f349-107">DESCRIPTION</span></span>
<span data-ttu-id="0f349-108">Polecenie cmdlet **Update-AzKeyVaultCertificate** modyfikuje atrybuty edytowalne certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0f349-108">The **Update-AzKeyVaultCertificate** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="0f349-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f349-109">EXAMPLES</span></span>

### <span data-ttu-id="0f349-110">Przykład 1. Modyfikowanie tagów skojarzonych z certyfikatem</span><span class="sxs-lookup"><span data-stu-id="0f349-110">Example 1: Modify the tags associated with a certificate</span></span>
```powershell
PS C:\> $Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Update-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags -PassThru

Name        : TestCert01
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Id          : https://ContosoKV01.vault.azure.net:443/certificates/TestCert01
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/TestCert01
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/TestCert01
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="0f349-111">Pierwsze polecenie powoduje przypisanie tablicy par klucz/wartość do zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="0f349-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="0f349-112">Drugie polecenie ustawia wartość znacznika certyfikatu o nazwie TestCert01 na $Tags.</span><span class="sxs-lookup"><span data-stu-id="0f349-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

## <span data-ttu-id="0f349-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f349-113">PARAMETERS</span></span>

### <span data-ttu-id="0f349-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f349-114">-DefaultProfile</span></span>
<span data-ttu-id="0f349-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f349-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f349-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="0f349-116">-Enable</span></span>
<span data-ttu-id="0f349-117">Jeśli jest obecny, Włącz certyfikat, jeśli wartość jest równa prawda.</span><span class="sxs-lookup"><span data-stu-id="0f349-117">If present, enable a certificate if value is true.</span></span>
<span data-ttu-id="0f349-118">Wyłącz certyfikat, jeśli wartość jest fałszywa.</span><span class="sxs-lookup"><span data-stu-id="0f349-118">Disable a certificate if value is false.</span></span>
<span data-ttu-id="0f349-119">Jeśli ta opcja nie jest określona, istniejąca wartość stanu (włączony/wyłączony) certyfikatu pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="0f349-119">If not specified, the existing value of the certificate's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f349-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0f349-120">-InputObject</span></span>
<span data-ttu-id="0f349-121">Obiekt Certificate</span><span class="sxs-lookup"><span data-stu-id="0f349-121">Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f349-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0f349-122">-Name</span></span>
<span data-ttu-id="0f349-123">Nazwa certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0f349-123">Certificate name.</span></span>
<span data-ttu-id="0f349-124">Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i sekretu.</span><span class="sxs-lookup"><span data-stu-id="0f349-124">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f349-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f349-125">-PassThru</span></span>
<span data-ttu-id="0f349-126">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="0f349-126">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="0f349-127">Jeśli ten przełącznik jest określony, zwracany jest obiekt certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0f349-127">If this switch is specified, return certificate object.</span></span>

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

### <span data-ttu-id="0f349-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="0f349-128">-Tag</span></span>
<span data-ttu-id="0f349-129">Obiekt Hashtable reprezentujący znaczniki certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0f349-129">A hashtable representing certificate tags.</span></span>
<span data-ttu-id="0f349-130">Jeśli nie podano tego parametru, istniejące znaczniki sertificate pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="0f349-130">If not specified, the existing tags of the sertificate remain unchanged.</span></span>
<span data-ttu-id="0f349-131">Usuń znacznik, określając pustą tablicę.</span><span class="sxs-lookup"><span data-stu-id="0f349-131">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f349-132">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="0f349-132">-VaultName</span></span>
<span data-ttu-id="0f349-133">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="0f349-133">Vault name.</span></span>
<span data-ttu-id="0f349-134">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="0f349-134">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="0f349-135">-Version</span><span class="sxs-lookup"><span data-stu-id="0f349-135">-Version</span></span>
<span data-ttu-id="0f349-136">Wersja certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0f349-136">Certificate version.</span></span>
<span data-ttu-id="0f349-137">Polecenie cmdlet tworzy nazwę FQDN certyfikatu na podstawie nazwy magazynu, obecnie wybranego środowiska, nazwy certyfikatu i wersji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0f349-137">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment, certificate name and certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f349-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f349-138">-Confirm</span></span>
<span data-ttu-id="0f349-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f349-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f349-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f349-140">-WhatIf</span></span>
<span data-ttu-id="0f349-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f349-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f349-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0f349-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f349-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f349-143">CommonParameters</span></span>
<span data-ttu-id="0f349-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f349-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f349-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f349-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f349-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f349-146">INPUTS</span></span>

### <span data-ttu-id="0f349-147">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0f349-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="0f349-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f349-148">OUTPUTS</span></span>

### <span data-ttu-id="0f349-149">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0f349-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="0f349-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f349-150">NOTES</span></span>

## <span data-ttu-id="0f349-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f349-151">RELATED LINKS</span></span>
