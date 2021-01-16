---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 298d6bac6b2c1b37cff47a22a1647caafdb3e843
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354925"
---
# <span data-ttu-id="8ac74-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8ac74-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="8ac74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ac74-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac74-103">Przywraca certyfikat w magazynie kluczy z pliku kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="8ac74-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="8ac74-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ac74-104">SYNTAX</span></span>

### <span data-ttu-id="8ac74-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8ac74-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac74-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ac74-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac74-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8ac74-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ac74-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8ac74-108">DESCRIPTION</span></span>
<span data-ttu-id="8ac74-109">Polecenie cmdlet **Restore-AzKeyVaultCertificate** tworzy certyfikat w określonym magazynie kluczy na podstawie pliku kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="8ac74-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="8ac74-110">Ten certyfikat jest repliką kopii zapasowej certyfikatu w pliku wejściowym i ma taką samą nazwę jak oryginalny certyfikat.</span><span class="sxs-lookup"><span data-stu-id="8ac74-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="8ac74-111">Jeśli magazyn kluczy zawiera już certyfikat o tej samej nazwie, nie powoduje to zastąpienia oryginalnego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8ac74-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="8ac74-112">Jeśli kopia zapasowa zawiera wiele wersji certyfikatu, wszystkie wersje zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="8ac74-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="8ac74-113">Magazyn kluczy, do którego zostanie przywrócony certyfikat, może różnić się od magazynu kluczy, z którego utworzono kopię zapasową certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8ac74-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="8ac74-114">Jednak Magazyn kluczy musi korzystać z tej samej subskrypcji i znajdować się w obszarze platformy Azure w tej samej geograficznej lokalizacji (na przykład w Ameryce Północnej).</span><span class="sxs-lookup"><span data-stu-id="8ac74-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="8ac74-115">Zobacz Centrum zaufania platformy Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) na potrzeby mapowania regionów usługi Azure na Geographies.</span><span class="sxs-lookup"><span data-stu-id="8ac74-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="8ac74-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ac74-116">EXAMPLES</span></span>

### <span data-ttu-id="8ac74-117">Przykład 1: Przywracanie kopii zapasowej certyfikatu</span><span class="sxs-lookup"><span data-stu-id="8ac74-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="8ac74-118">To polecenie przywraca certyfikat, w tym wszystkie jego wersje, z pliku kopii zapasowej o nazwie Backup. blob do magazynu kluczy o nazwie MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="8ac74-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="8ac74-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ac74-119">PARAMETERS</span></span>

### <span data-ttu-id="8ac74-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac74-120">-DefaultProfile</span></span>
<span data-ttu-id="8ac74-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac74-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ac74-122">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="8ac74-122">-InputFile</span></span>
<span data-ttu-id="8ac74-123">Plik wejściowy.</span><span class="sxs-lookup"><span data-stu-id="8ac74-123">Input file.</span></span>
<span data-ttu-id="8ac74-124">Plik wejściowy zawierający obiekt BLOB z kopią zapasową</span><span class="sxs-lookup"><span data-stu-id="8ac74-124">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="8ac74-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ac74-125">-InputObject</span></span>
<span data-ttu-id="8ac74-126">Obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="8ac74-126">KeyVault object</span></span>

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

### <span data-ttu-id="8ac74-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ac74-127">-ResourceId</span></span>
<span data-ttu-id="8ac74-128">Identyfikator zasobu magazynu</span><span class="sxs-lookup"><span data-stu-id="8ac74-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="8ac74-129">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="8ac74-129">-VaultName</span></span>
<span data-ttu-id="8ac74-130">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="8ac74-130">Vault name.</span></span>
<span data-ttu-id="8ac74-131">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="8ac74-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8ac74-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ac74-132">-Confirm</span></span>
<span data-ttu-id="8ac74-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac74-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ac74-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ac74-134">-WhatIf</span></span>
<span data-ttu-id="8ac74-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac74-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ac74-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8ac74-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ac74-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac74-137">CommonParameters</span></span>
<span data-ttu-id="8ac74-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac74-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac74-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ac74-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac74-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ac74-140">INPUTS</span></span>

### <span data-ttu-id="8ac74-141">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8ac74-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8ac74-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8ac74-142">System.String</span></span>

## <span data-ttu-id="8ac74-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ac74-143">OUTPUTS</span></span>

### <span data-ttu-id="8ac74-144">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8ac74-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="8ac74-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ac74-145">NOTES</span></span>

## <span data-ttu-id="8ac74-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ac74-146">RELATED LINKS</span></span>
