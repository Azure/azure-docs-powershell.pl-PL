---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188875"
---
# <span data-ttu-id="e43ca-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="e43ca-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="e43ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e43ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e43ca-103">Wyłącza zasady przywracania obiektów blob na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="e43ca-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="e43ca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e43ca-104">SYNTAX</span></span>

### <span data-ttu-id="e43ca-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="e43ca-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e43ca-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e43ca-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e43ca-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="e43ca-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e43ca-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e43ca-108">DESCRIPTION</span></span>
<span data-ttu-id="e43ca-109">Polecenie **cmdlet Disable-AzStorageBlobRestorePolicy** wyłącza zasady przywracania obiektów blob dla usługi obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e43ca-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="e43ca-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e43ca-110">EXAMPLES</span></span>

### <span data-ttu-id="e43ca-111">Przykład 1. Wyłącza zasady przywracania obiektów blob dla usługi obiektów blob magazynu platformy Azure na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="e43ca-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="e43ca-112">To polecenie wyłącza zasady przywracania obiektów blob dla usługi obiektów blob magazynu platformy Azure na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="e43ca-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="e43ca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e43ca-113">PARAMETERS</span></span>

### <span data-ttu-id="e43ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43ca-114">-DefaultProfile</span></span>
<span data-ttu-id="e43ca-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e43ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e43ca-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e43ca-116">-PassThru</span></span>
<span data-ttu-id="e43ca-117">Wyświetl właściwości usługi</span><span class="sxs-lookup"><span data-stu-id="e43ca-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="e43ca-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e43ca-118">-ResourceGroupName</span></span>
<span data-ttu-id="e43ca-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e43ca-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="e43ca-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e43ca-120">-ResourceId</span></span>
<span data-ttu-id="e43ca-121">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="e43ca-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43ca-122">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e43ca-122">-StorageAccount</span></span>
<span data-ttu-id="e43ca-123">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="e43ca-123">Storage account object</span></span>

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

### <span data-ttu-id="e43ca-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e43ca-124">-StorageAccountName</span></span>
<span data-ttu-id="e43ca-125">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e43ca-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="e43ca-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e43ca-126">-Confirm</span></span>
<span data-ttu-id="e43ca-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e43ca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e43ca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e43ca-128">-WhatIf</span></span>
<span data-ttu-id="e43ca-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e43ca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e43ca-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e43ca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e43ca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43ca-131">CommonParameters</span></span>
<span data-ttu-id="e43ca-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e43ca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43ca-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e43ca-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43ca-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e43ca-134">INPUTS</span></span>

### <span data-ttu-id="e43ca-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e43ca-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e43ca-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e43ca-136">System.String</span></span>

## <span data-ttu-id="e43ca-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e43ca-137">OUTPUTS</span></span>

### <span data-ttu-id="e43ca-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="e43ca-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="e43ca-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e43ca-139">NOTES</span></span>

## <span data-ttu-id="e43ca-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e43ca-140">RELATED LINKS</span></span>
