---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491245"
---
# <span data-ttu-id="495aa-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="495aa-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="495aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="495aa-102">SYNOPSIS</span></span>
<span data-ttu-id="495aa-103">Modyfikuje właściwości usługi dla usługi plików magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="495aa-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="495aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="495aa-104">SYNTAX</span></span>

### <span data-ttu-id="495aa-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="495aa-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="495aa-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="495aa-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="495aa-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="495aa-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="495aa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="495aa-108">DESCRIPTION</span></span>
<span data-ttu-id="495aa-109">Polecenie cmdlet **Update-AzStorageFileServiceProperty** modyfikuje właściwości usługi dla usługi plików magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="495aa-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="495aa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="495aa-110">EXAMPLES</span></span>

### <span data-ttu-id="495aa-111">Przykład 1: Włączanie softdelete udostępniania plików</span><span class="sxs-lookup"><span data-stu-id="495aa-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="495aa-112">To polecenie umożliwia udostępnianie plików softdelete usuwanie z uwzględnieniem dni przechowywania w liczbie 5</span><span class="sxs-lookup"><span data-stu-id="495aa-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="495aa-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="495aa-113">PARAMETERS</span></span>

### <span data-ttu-id="495aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495aa-114">-DefaultProfile</span></span>
<span data-ttu-id="495aa-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="495aa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="495aa-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="495aa-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="495aa-117">Włączanie udostępniania usuwanie zasad przechowywania dla konta magazynu według ustawienia $true, wyłącz opcję Udostępnij zasady przechowywania według ustawienia $false.</span><span class="sxs-lookup"><span data-stu-id="495aa-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495aa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="495aa-118">-ResourceGroupName</span></span>
<span data-ttu-id="495aa-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="495aa-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495aa-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="495aa-120">-ResourceId</span></span>
<span data-ttu-id="495aa-121">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi plików.</span><span class="sxs-lookup"><span data-stu-id="495aa-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="495aa-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="495aa-122">-ShareRetentionDays</span></span>
<span data-ttu-id="495aa-123">Ustawia liczbę dni przechowywania dla DeleteRetentionPolicy udziału.</span><span class="sxs-lookup"><span data-stu-id="495aa-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="495aa-124">Wartość powinna być ustawiana tylko w przypadku włączenia zasad przechowywania udostępniania i usuwania.</span><span class="sxs-lookup"><span data-stu-id="495aa-124">The value should only be set when enable share Delete Retention Policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days, RetentionDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495aa-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="495aa-125">-StorageAccount</span></span>
<span data-ttu-id="495aa-126">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="495aa-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="495aa-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="495aa-127">-StorageAccountName</span></span>
<span data-ttu-id="495aa-128">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="495aa-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495aa-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="495aa-129">-Confirm</span></span>
<span data-ttu-id="495aa-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="495aa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="495aa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="495aa-131">-WhatIf</span></span>
<span data-ttu-id="495aa-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="495aa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="495aa-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="495aa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="495aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495aa-134">CommonParameters</span></span>
<span data-ttu-id="495aa-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="495aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495aa-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="495aa-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495aa-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="495aa-137">INPUTS</span></span>

### <span data-ttu-id="495aa-138">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="495aa-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="495aa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="495aa-139">System.String</span></span>

## <span data-ttu-id="495aa-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="495aa-140">OUTPUTS</span></span>

### <span data-ttu-id="495aa-141">Microsoft. Azure. Commands. Management. Storage. models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="495aa-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="495aa-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="495aa-142">NOTES</span></span>

## <span data-ttu-id="495aa-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="495aa-143">RELATED LINKS</span></span>
