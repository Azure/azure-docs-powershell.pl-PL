---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 12e1844be497baa24a3b9b4aa9c4e5690564f4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527926"
---
# <span data-ttu-id="549c1-101">Restore-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="549c1-101">Restore-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="549c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="549c1-102">SYNOPSIS</span></span>
<span data-ttu-id="549c1-103">Przywraca zarządzane konto magazynu w magazynie kluczy z pliku kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="549c1-103">Restores a managed storage account in a key vault from a backup file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="549c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="549c1-104">SYNTAX</span></span>

### <span data-ttu-id="549c1-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="549c1-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="549c1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="549c1-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="549c1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="549c1-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="549c1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="549c1-108">DESCRIPTION</span></span>
<span data-ttu-id="549c1-109">Polecenie cmdlet **Restore-AzureKeyVaultManagedStorageAccount** tworzy zarządzane konto magazynu w określonym magazynie kluczy na podstawie pliku kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="549c1-109">The **Restore-AzureKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="549c1-110">To konto zarządzanej przestrzeni dyskowej to replika z kopią zapasową zarządzanych kont magazynu w pliku wejściowym i ma taką samą nazwę jak oryginalna.</span><span class="sxs-lookup"><span data-stu-id="549c1-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="549c1-111">Jeśli magazyn kluczy zawiera już zarządzane konto magazynu o tej samej nazwie, zamiast zastępowania oryginału nie jest wyświetlane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="549c1-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="549c1-112">Magazyn kluczy, do którego jest przywracane konto zarządzanego magazynu, może różnić się od magazynu kluczy, z którego utworzono kopię zapasową zarządzanego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="549c1-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="549c1-113">Jednak Magazyn kluczy musi korzystać z tej samej subskrypcji i znajdować się w obszarze platformy Azure w tej samej geograficznej lokalizacji (na przykład w Ameryce Północnej).</span><span class="sxs-lookup"><span data-stu-id="549c1-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="549c1-114">Zobacz Centrum zaufania platformy Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) na potrzeby mapowania regionów usługi Azure na Geographies.</span><span class="sxs-lookup"><span data-stu-id="549c1-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="549c1-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="549c1-115">EXAMPLES</span></span>

### <span data-ttu-id="549c1-116">Przykład 1: Przywracanie kopii zapasowej zarządzanych kont magazynu</span><span class="sxs-lookup"><span data-stu-id="549c1-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Id                  : https://mykeyvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : MyKeyVault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="549c1-117">To polecenie przywraca zarządzane konto magazynu, w tym wszystkie jego wersje, z pliku kopii zapasowej o nazwie Backup. blob do magazynu kluczy o nazwie MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="549c1-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="549c1-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="549c1-118">PARAMETERS</span></span>

### <span data-ttu-id="549c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="549c1-119">-DefaultProfile</span></span>
<span data-ttu-id="549c1-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="549c1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="549c1-121">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="549c1-121">-InputFile</span></span>
<span data-ttu-id="549c1-122">Plik wejściowy.</span><span class="sxs-lookup"><span data-stu-id="549c1-122">Input file.</span></span>
<span data-ttu-id="549c1-123">Plik wejściowy zawierający obiekt BLOB z kopią zapasową</span><span class="sxs-lookup"><span data-stu-id="549c1-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="549c1-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="549c1-124">-InputObject</span></span>
<span data-ttu-id="549c1-125">Obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="549c1-125">KeyVault object</span></span>

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

### <span data-ttu-id="549c1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="549c1-126">-ResourceId</span></span>
<span data-ttu-id="549c1-127">Identyfikator zasobu magazynu</span><span class="sxs-lookup"><span data-stu-id="549c1-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="549c1-128">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="549c1-128">-VaultName</span></span>
<span data-ttu-id="549c1-129">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="549c1-129">Vault name.</span></span>
<span data-ttu-id="549c1-130">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="549c1-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="549c1-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="549c1-131">-Confirm</span></span>
<span data-ttu-id="549c1-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="549c1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="549c1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="549c1-133">-WhatIf</span></span>
<span data-ttu-id="549c1-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="549c1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="549c1-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="549c1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="549c1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="549c1-136">CommonParameters</span></span>
<span data-ttu-id="549c1-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="549c1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="549c1-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="549c1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="549c1-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="549c1-139">INPUTS</span></span>

### <span data-ttu-id="549c1-140">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="549c1-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="549c1-141">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="549c1-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="549c1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="549c1-142">System.String</span></span>

## <span data-ttu-id="549c1-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="549c1-143">OUTPUTS</span></span>

### <span data-ttu-id="549c1-144">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="549c1-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="549c1-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="549c1-145">NOTES</span></span>

## <span data-ttu-id="549c1-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="549c1-146">RELATED LINKS</span></span>
