---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 136469819a43dbb918aefebd8134b38ef4a943c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952474"
---
# <span data-ttu-id="24840-101">Restore-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24840-101">Restore-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="24840-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24840-102">SYNOPSIS</span></span>
<span data-ttu-id="24840-103">Przywraca konto magazynu zarządzanego w magazynie kluczy z pliku kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="24840-103">Restores a managed storage account in a key vault from a backup file.</span></span>

## <span data-ttu-id="24840-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="24840-104">SYNTAX</span></span>

### <span data-ttu-id="24840-105">ByVaultName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="24840-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24840-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="24840-106">ByInputObject</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24840-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24840-107">ByResourceId</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24840-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="24840-108">DESCRIPTION</span></span>
<span data-ttu-id="24840-109">Polecenie **cmdlet Restore-AzKeyVaultManagedStorageAccount** tworzy konto magazynu zarządzanego w określonym magazynie kluczy z pliku kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="24840-109">The **Restore-AzKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="24840-110">To konto magazynu zarządzanego jest repliką kopii zapasowej zarządzanego konta magazynu w pliku wejściowym i ma taką samą nazwę jak oryginał.</span><span class="sxs-lookup"><span data-stu-id="24840-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="24840-111">Jeśli magazyn kluczy zawiera już konto magazynu zarządzanego o tej samej nazwie, to polecenie cmdlet kończy się niepowodzeniem, zamiast zapełniać oryginał.</span><span class="sxs-lookup"><span data-stu-id="24840-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="24840-112">Magazyn kluczy, z którym przywracasz konto magazynu zarządzanego, może różnić się od magazynu kluczy, z którym jest tworzyć kopię zapasową konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="24840-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="24840-113">Jednak magazyn kluczy musi korzystać z tej samej subskrypcji i znajdować się w regionie platformy Azure w tej samej lokalizacji geograficznej (na przykład Ameryki Północnej).</span><span class="sxs-lookup"><span data-stu-id="24840-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="24840-114">Zobacz Centrum zaufania platformy Microsoft Azure (aby uzyskać informacje na temat mapowania regionów https://azure.microsoft.com/support/trust-center/) platformy Azure na obszary geograficzne).</span><span class="sxs-lookup"><span data-stu-id="24840-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="24840-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="24840-115">EXAMPLES</span></span>

### <span data-ttu-id="24840-116">Przykład 1. Przywracanie kopii zapasowej zarządzanego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="24840-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="24840-117">To polecenie przywraca zarządzane konto magazynu, łącznie ze wszystkimi jego wersjami, z pliku kopii zapasowej o nazwie Backup.blob do magazynu kluczy o nazwie MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="24840-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="24840-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24840-118">PARAMETERS</span></span>

### <span data-ttu-id="24840-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24840-119">-DefaultProfile</span></span>
<span data-ttu-id="24840-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="24840-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24840-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="24840-121">-InputFile</span></span>
<span data-ttu-id="24840-122">Plik wejściowy.</span><span class="sxs-lookup"><span data-stu-id="24840-122">Input file.</span></span>
<span data-ttu-id="24840-123">Plik wejściowy zawierający obiekt blob kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="24840-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="24840-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24840-124">-InputObject</span></span>
<span data-ttu-id="24840-125">Obiekt KeyVault</span><span class="sxs-lookup"><span data-stu-id="24840-125">KeyVault object</span></span>

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

### <span data-ttu-id="24840-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24840-126">-ResourceId</span></span>
<span data-ttu-id="24840-127">Identyfikator zasobu KeyVault</span><span class="sxs-lookup"><span data-stu-id="24840-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="24840-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="24840-128">-VaultName</span></span>
<span data-ttu-id="24840-129">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="24840-129">Vault name.</span></span>
<span data-ttu-id="24840-130">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="24840-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="24840-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24840-131">-Confirm</span></span>
<span data-ttu-id="24840-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="24840-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24840-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24840-133">-WhatIf</span></span>
<span data-ttu-id="24840-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24840-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24840-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="24840-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24840-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24840-136">CommonParameters</span></span>
<span data-ttu-id="24840-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24840-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24840-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24840-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24840-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24840-139">INPUTS</span></span>

### <span data-ttu-id="24840-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="24840-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="24840-141">System.String</span><span class="sxs-lookup"><span data-stu-id="24840-141">System.String</span></span>

## <span data-ttu-id="24840-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24840-142">OUTPUTS</span></span>

### <span data-ttu-id="24840-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24840-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="24840-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="24840-144">NOTES</span></span>

## <span data-ttu-id="24840-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24840-145">RELATED LINKS</span></span>
