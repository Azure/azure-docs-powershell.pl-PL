---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: ebb379217f9fd040aa3dcbd6c614a45dbdbba8c4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374143"
---
# <span data-ttu-id="9c1bb-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9c1bb-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="9c1bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c1bb-102">SYNOPSIS</span></span>
<span data-ttu-id="9c1bb-103">Włącz zasady dotyczące przechowywania obiektów BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="9c1bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c1bb-104">SYNTAX</span></span>

### <span data-ttu-id="9c1bb-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9c1bb-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c1bb-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="9c1bb-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c1bb-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="9c1bb-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c1bb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9c1bb-108">DESCRIPTION</span></span>
<span data-ttu-id="9c1bb-109">Polecenie cmdlet **enable-AzStorageBlobDeleteRetentionPolicy** umożliwia usuwanie zasad przechowywania dla usługi blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="9c1bb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c1bb-110">EXAMPLES</span></span>

### <span data-ttu-id="9c1bb-111">Przykład 1: Włączanie zasad usuwania dotyczących przechowywania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="9c1bb-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="9c1bb-112">To polecenie umożliwia usuwanie zasad przechowywania dla usługi BLOB i Ustawianie usunięte dni przechowywania obiektów BLOB na wartość 4.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="9c1bb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c1bb-113">PARAMETERS</span></span>

### <span data-ttu-id="9c1bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c1bb-114">-DefaultProfile</span></span>
<span data-ttu-id="9c1bb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c1bb-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c1bb-116">-PassThru</span></span>
<span data-ttu-id="9c1bb-117">Wyświetlanie właściwości serviceproperties</span><span class="sxs-lookup"><span data-stu-id="9c1bb-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="9c1bb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c1bb-118">-ResourceGroupName</span></span>
<span data-ttu-id="9c1bb-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="9c1bb-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c1bb-120">-ResourceId</span></span>
<span data-ttu-id="9c1bb-121">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="9c1bb-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="9c1bb-122">-RetentionDays</span></span>
<span data-ttu-id="9c1bb-123">Umożliwia ustawienie liczby dni przechowywania dla DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c1bb-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9c1bb-124">-StorageAccount</span></span>
<span data-ttu-id="9c1bb-125">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="9c1bb-125">Storage account object</span></span>

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

### <span data-ttu-id="9c1bb-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9c1bb-126">-StorageAccountName</span></span>
<span data-ttu-id="9c1bb-127">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="9c1bb-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c1bb-128">-Confirm</span></span>
<span data-ttu-id="9c1bb-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c1bb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c1bb-130">-WhatIf</span></span>
<span data-ttu-id="9c1bb-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c1bb-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c1bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c1bb-133">CommonParameters</span></span>
<span data-ttu-id="9c1bb-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c1bb-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c1bb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c1bb-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c1bb-136">INPUTS</span></span>

### <span data-ttu-id="9c1bb-137">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9c1bb-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="9c1bb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9c1bb-138">System.String</span></span>

## <span data-ttu-id="9c1bb-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c1bb-139">OUTPUTS</span></span>

### <span data-ttu-id="9c1bb-140">Microsoft. Azure. Commands. Management. Storage. models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="9c1bb-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="9c1bb-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c1bb-141">NOTES</span></span>

## <span data-ttu-id="9c1bb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c1bb-142">RELATED LINKS</span></span>
