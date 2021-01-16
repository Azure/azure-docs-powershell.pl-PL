---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: ebb379217f9fd040aa3dcbd6c614a45dbdbba8c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349798"
---
# <span data-ttu-id="7b0d3-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7b0d3-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="7b0d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b0d3-102">SYNOPSIS</span></span>
<span data-ttu-id="7b0d3-103">Włącz zasady dotyczące przechowywania obiektów BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7b0d3-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="7b0d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b0d3-104">SYNTAX</span></span>

### <span data-ttu-id="7b0d3-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7b0d3-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b0d3-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="7b0d3-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b0d3-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="7b0d3-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b0d3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7b0d3-108">DESCRIPTION</span></span>
<span data-ttu-id="7b0d3-109">Polecenie cmdlet **enable-AzStorageBlobDeleteRetentionPolicy** umożliwia usuwanie zasad przechowywania dla usługi blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="7b0d3-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="7b0d3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b0d3-110">EXAMPLES</span></span>

### <span data-ttu-id="7b0d3-111">Przykład 1: Włączanie zasad usuwania dotyczących przechowywania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="7b0d3-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="7b0d3-112">To polecenie umożliwia usuwanie zasad przechowywania dla usługi BLOB i Ustawianie usunięte dni przechowywania obiektów BLOB na wartość 4.</span><span class="sxs-lookup"><span data-stu-id="7b0d3-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="7b0d3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b0d3-113">PARAMETERS</span></span>

### <span data-ttu-id="7b0d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b0d3-114">-DefaultProfile</span></span>
<span data-ttu-id="7b0d3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b0d3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b0d3-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b0d3-116">-PassThru</span></span>
<span data-ttu-id="7b0d3-117">Wyświetlanie właściwości serviceproperties</span><span class="sxs-lookup"><span data-stu-id="7b0d3-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="7b0d3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b0d3-118">-ResourceGroupName</span></span>
<span data-ttu-id="7b0d3-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b0d3-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="7b0d3-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b0d3-120">-ResourceId</span></span>
<span data-ttu-id="7b0d3-121">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="7b0d3-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="7b0d3-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="7b0d3-122">-RetentionDays</span></span>
<span data-ttu-id="7b0d3-123">Umożliwia ustawienie liczby dni przechowywania dla DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="7b0d3-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="7b0d3-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b0d3-124">-StorageAccount</span></span>
<span data-ttu-id="7b0d3-125">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="7b0d3-125">Storage account object</span></span>

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

### <span data-ttu-id="7b0d3-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7b0d3-126">-StorageAccountName</span></span>
<span data-ttu-id="7b0d3-127">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7b0d3-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="7b0d3-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b0d3-128">-Confirm</span></span>
<span data-ttu-id="7b0d3-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b0d3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b0d3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b0d3-130">-WhatIf</span></span>
<span data-ttu-id="7b0d3-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b0d3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b0d3-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b0d3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b0d3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b0d3-133">CommonParameters</span></span>
<span data-ttu-id="7b0d3-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b0d3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b0d3-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b0d3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b0d3-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b0d3-136">INPUTS</span></span>

### <span data-ttu-id="7b0d3-137">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b0d3-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="7b0d3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7b0d3-138">System.String</span></span>

## <span data-ttu-id="7b0d3-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b0d3-139">OUTPUTS</span></span>

### <span data-ttu-id="7b0d3-140">Microsoft. Azure. Commands. Management. Storage. models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="7b0d3-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="7b0d3-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b0d3-141">NOTES</span></span>

## <span data-ttu-id="7b0d3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b0d3-142">RELATED LINKS</span></span>
