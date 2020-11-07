---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7955ecd02d40ac3dff891b8eb315a39ccf985ebb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719122"
---
# <span data-ttu-id="13869-101">Restore-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="13869-101">Restore-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="13869-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13869-102">SYNOPSIS</span></span>
<span data-ttu-id="13869-103">Przywraca certyfikat w magazynie kluczy z pliku kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="13869-103">Restores a certificate in a key vault from a backup file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13869-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13869-104">SYNTAX</span></span>

### <span data-ttu-id="13869-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="13869-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13869-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="13869-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13869-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13869-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13869-108">Opis</span><span class="sxs-lookup"><span data-stu-id="13869-108">DESCRIPTION</span></span>
<span data-ttu-id="13869-109">Polecenie cmdlet **Restore-AzureKeyVaultCertificate** tworzy certyfikat w określonym magazynie kluczy na podstawie pliku kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="13869-109">The **Restore-AzureKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="13869-110">Ten certyfikat jest repliką kopii zapasowej certyfikatu w pliku wejściowym i ma taką samą nazwę jak oryginalny certyfikat.</span><span class="sxs-lookup"><span data-stu-id="13869-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="13869-111">Jeśli magazyn kluczy zawiera już certyfikat o tej samej nazwie, nie powoduje to zastąpienia oryginalnego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="13869-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="13869-112">Jeśli kopia zapasowa zawiera wiele wersji certyfikatu, wszystkie wersje zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="13869-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="13869-113">Magazyn kluczy, do którego zostanie przywrócony certyfikat, może różnić się od magazynu kluczy, z którego utworzono kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="13869-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="13869-114">Jednak Magazyn kluczy musi korzystać z tej samej subskrypcji i znajdować się w obszarze platformy Azure w tej samej geograficznej lokalizacji (na przykład w Ameryce Północnej).</span><span class="sxs-lookup"><span data-stu-id="13869-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="13869-115">Zobacz Centrum zaufania platformy Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) na potrzeby mapowania regionów usługi Azure na Geographies.</span><span class="sxs-lookup"><span data-stu-id="13869-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="13869-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13869-116">EXAMPLES</span></span>

### <span data-ttu-id="13869-117">Przykład 1: Przywracanie kopii zapasowej certyfikatu</span><span class="sxs-lookup"><span data-stu-id="13869-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/25/2018 3:47:41 AM

                [Not After]
                  11/25/2018 2:57:41 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Purgeable
Enabled       : True
Expires       : 11/25/2018 10:57:41 AM
NotBefore     : 5/25/2018 10:47:41 AM
Created       : 5/25/2018 10:57:41 AM
Updated       : 5/25/2018 10:57:41 AM
Tags          : 
VaultName     : MyKeyVault
Name          : cert1
Version       : bd406f6d6b3a41a1a1c633494d8c3c3a
Id            : https://mykeyvault.vault.azure.net:443/certificates/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
```

<span data-ttu-id="13869-118">To polecenie przywraca certyfikat, w tym wszystkie jego wersje, z pliku kopii zapasowej o nazwie Backup. blob do magazynu kluczy o nazwie MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="13869-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="13869-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13869-119">PARAMETERS</span></span>

### <span data-ttu-id="13869-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13869-120">-DefaultProfile</span></span>
<span data-ttu-id="13869-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13869-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13869-122">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="13869-122">-InputFile</span></span>
<span data-ttu-id="13869-123">Plik wejściowy.</span><span class="sxs-lookup"><span data-stu-id="13869-123">Input file.</span></span>
<span data-ttu-id="13869-124">Plik wejściowy zawierający obiekt BLOB z kopią zapasową</span><span class="sxs-lookup"><span data-stu-id="13869-124">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13869-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="13869-125">-InputObject</span></span>
<span data-ttu-id="13869-126">Obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="13869-126">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13869-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13869-127">-ResourceId</span></span>
<span data-ttu-id="13869-128">Identyfikator zasobu magazynu</span><span class="sxs-lookup"><span data-stu-id="13869-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="13869-129">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="13869-129">-VaultName</span></span>
<span data-ttu-id="13869-130">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="13869-130">Vault name.</span></span>
<span data-ttu-id="13869-131">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="13869-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13869-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13869-132">-Confirm</span></span>
<span data-ttu-id="13869-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13869-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13869-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13869-134">-WhatIf</span></span>
<span data-ttu-id="13869-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13869-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13869-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13869-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13869-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13869-137">CommonParameters</span></span>
<span data-ttu-id="13869-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13869-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13869-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13869-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13869-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13869-140">INPUTS</span></span>

### <span data-ttu-id="13869-141">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="13869-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="13869-142">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13869-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="13869-143">System. String</span><span class="sxs-lookup"><span data-stu-id="13869-143">System.String</span></span>

## <span data-ttu-id="13869-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13869-144">OUTPUTS</span></span>

### <span data-ttu-id="13869-145">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="13869-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="13869-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13869-146">NOTES</span></span>

## <span data-ttu-id="13869-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13869-147">RELATED LINKS</span></span>
