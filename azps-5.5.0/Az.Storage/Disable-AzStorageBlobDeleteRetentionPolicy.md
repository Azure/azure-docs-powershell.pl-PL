---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188882"
---
# <span data-ttu-id="24171-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="24171-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="24171-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24171-102">SYNOPSIS</span></span>
<span data-ttu-id="24171-103">Wyłącz zasady przechowywania usuwania dla usługi obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="24171-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="24171-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="24171-104">SYNTAX</span></span>

### <span data-ttu-id="24171-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="24171-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24171-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="24171-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24171-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="24171-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24171-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="24171-108">DESCRIPTION</span></span>
<span data-ttu-id="24171-109">Polecenie cmdlet **Disable-AzStorageBlobDeleteRetentionPolicy** wyłącza zasady przechowywania usuwania dla usługi obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="24171-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="24171-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="24171-110">EXAMPLES</span></span>

### <span data-ttu-id="24171-111">Przykład 1. Wyłączanie zasad przechowywania usuwania dla usługi obiektów blob</span><span class="sxs-lookup"><span data-stu-id="24171-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="24171-112">To polecenie wyłącza zasady przechowywania usuwania dla usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="24171-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="24171-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24171-113">PARAMETERS</span></span>

### <span data-ttu-id="24171-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24171-114">-DefaultProfile</span></span>
<span data-ttu-id="24171-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="24171-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24171-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24171-116">-PassThru</span></span>
<span data-ttu-id="24171-117">Wyświetlanie właściwości usługi</span><span class="sxs-lookup"><span data-stu-id="24171-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="24171-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24171-118">-ResourceGroupName</span></span>
<span data-ttu-id="24171-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="24171-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="24171-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24171-120">-ResourceId</span></span>
<span data-ttu-id="24171-121">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="24171-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="24171-122">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="24171-122">-StorageAccount</span></span>
<span data-ttu-id="24171-123">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="24171-123">Storage account object</span></span>

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

### <span data-ttu-id="24171-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="24171-124">-StorageAccountName</span></span>
<span data-ttu-id="24171-125">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="24171-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="24171-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24171-126">-Confirm</span></span>
<span data-ttu-id="24171-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="24171-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24171-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24171-128">-WhatIf</span></span>
<span data-ttu-id="24171-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24171-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24171-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="24171-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24171-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24171-131">CommonParameters</span></span>
<span data-ttu-id="24171-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24171-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24171-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24171-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24171-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24171-134">INPUTS</span></span>

### <span data-ttu-id="24171-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24171-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="24171-136">System.String</span><span class="sxs-lookup"><span data-stu-id="24171-136">System.String</span></span>

## <span data-ttu-id="24171-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24171-137">OUTPUTS</span></span>

### <span data-ttu-id="24171-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="24171-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="24171-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="24171-139">NOTES</span></span>

## <span data-ttu-id="24171-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24171-140">RELATED LINKS</span></span>
