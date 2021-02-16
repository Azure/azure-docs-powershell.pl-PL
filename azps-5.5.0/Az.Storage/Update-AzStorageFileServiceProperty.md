---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197467"
---
# <span data-ttu-id="6bf07-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6bf07-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="6bf07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bf07-102">SYNOPSIS</span></span>
<span data-ttu-id="6bf07-103">Modyfikuje właściwości usługi dla usługi plików magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6bf07-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="6bf07-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6bf07-104">SYNTAX</span></span>

### <span data-ttu-id="6bf07-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="6bf07-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bf07-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6bf07-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bf07-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="6bf07-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bf07-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6bf07-108">DESCRIPTION</span></span>
<span data-ttu-id="6bf07-109">Polecenie cmdlet **Update-AzStorageFileServiceProperty** modyfikuje właściwości usługi dla usługi plików magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6bf07-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="6bf07-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6bf07-110">EXAMPLES</span></span>

### <span data-ttu-id="6bf07-111">Przykład 1. Włączanie funkcji "softdelete" udziału plików</span><span class="sxs-lookup"><span data-stu-id="6bf07-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="6bf07-112">To polecenie umożliwia usuwanie softdelete udziału plików z dniem przechowywania 5</span><span class="sxs-lookup"><span data-stu-id="6bf07-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="6bf07-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bf07-113">PARAMETERS</span></span>

### <span data-ttu-id="6bf07-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bf07-114">-DefaultProfile</span></span>
<span data-ttu-id="6bf07-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6bf07-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bf07-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6bf07-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="6bf07-117">Włącz zasady przechowywania usuwania udostępniania dla konta magazynu przez ustawienie $true, wyłącz zasady przechowywania usuwania udostępniania przez ustawienie $false.</span><span class="sxs-lookup"><span data-stu-id="6bf07-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

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

### <span data-ttu-id="6bf07-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bf07-118">-ResourceGroupName</span></span>
<span data-ttu-id="6bf07-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bf07-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="6bf07-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bf07-120">-ResourceId</span></span>
<span data-ttu-id="6bf07-121">Wprowadź identyfikator zasobu konta magazynu lub właściwości usługi plików identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="6bf07-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="6bf07-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="6bf07-122">-ShareRetentionDays</span></span>
<span data-ttu-id="6bf07-123">Ustawia liczbę dni przechowywania dla akcji DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="6bf07-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="6bf07-124">Wartość powinna być ustawiana tylko po włączeniu zasad przechowywania usuwania udostępniania.</span><span class="sxs-lookup"><span data-stu-id="6bf07-124">The value should only be set when enable share Delete Retention Policy.</span></span>

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

### <span data-ttu-id="6bf07-125">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6bf07-125">-StorageAccount</span></span>
<span data-ttu-id="6bf07-126">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="6bf07-126">Storage account object</span></span>

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

### <span data-ttu-id="6bf07-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6bf07-127">-StorageAccountName</span></span>
<span data-ttu-id="6bf07-128">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6bf07-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="6bf07-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6bf07-129">-Confirm</span></span>
<span data-ttu-id="6bf07-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6bf07-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bf07-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bf07-131">-WhatIf</span></span>
<span data-ttu-id="6bf07-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bf07-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bf07-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6bf07-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bf07-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bf07-134">CommonParameters</span></span>
<span data-ttu-id="6bf07-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bf07-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bf07-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bf07-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bf07-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bf07-137">INPUTS</span></span>

### <span data-ttu-id="6bf07-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6bf07-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6bf07-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6bf07-139">System.String</span></span>

## <span data-ttu-id="6bf07-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bf07-140">OUTPUTS</span></span>

### <span data-ttu-id="6bf07-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="6bf07-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="6bf07-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6bf07-142">NOTES</span></span>

## <span data-ttu-id="6bf07-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bf07-143">RELATED LINKS</span></span>
