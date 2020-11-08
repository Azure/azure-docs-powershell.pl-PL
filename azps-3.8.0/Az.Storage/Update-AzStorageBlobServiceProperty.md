---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: b7d6299af3f56dd8f09c73171ab6630cbbb9bc96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051490"
---
# <span data-ttu-id="18fc8-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="18fc8-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="18fc8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="18fc8-103">Modyfikuje właściwości usługi dla usługi blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="18fc8-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="18fc8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18fc8-104">SYNTAX</span></span>

### <span data-ttu-id="18fc8-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="18fc8-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18fc8-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="18fc8-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18fc8-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="18fc8-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18fc8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="18fc8-108">DESCRIPTION</span></span>
<span data-ttu-id="18fc8-109">Polecenie cmdlet **Update-AzStorageBlobServiceProperty** modyfikuje właściwości usługi dla usługi blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="18fc8-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="18fc8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18fc8-110">EXAMPLES</span></span>

### <span data-ttu-id="18fc8-111">Przykład 1: Ustawianie DefaultServiceVersion usługi BLOB na 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="18fc8-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False                                                   
```

<span data-ttu-id="18fc8-112">To polecenie ustawia DefaultServiceVersion usługi BLOB na 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="18fc8-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

## <span data-ttu-id="18fc8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18fc8-113">PARAMETERS</span></span>

### <span data-ttu-id="18fc8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18fc8-114">-DefaultProfile</span></span>
<span data-ttu-id="18fc8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18fc8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18fc8-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="18fc8-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="18fc8-117">Domyślna wersja usługi do ustawienia</span><span class="sxs-lookup"><span data-stu-id="18fc8-117">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fc8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18fc8-118">-ResourceGroupName</span></span>
<span data-ttu-id="18fc8-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="18fc8-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="18fc8-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18fc8-120">-ResourceId</span></span>
<span data-ttu-id="18fc8-121">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="18fc8-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="18fc8-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="18fc8-122">-StorageAccount</span></span>
<span data-ttu-id="18fc8-123">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="18fc8-123">Storage account object</span></span>

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

### <span data-ttu-id="18fc8-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="18fc8-124">-StorageAccountName</span></span>
<span data-ttu-id="18fc8-125">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="18fc8-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="18fc8-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="18fc8-126">-Confirm</span></span>
<span data-ttu-id="18fc8-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18fc8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18fc8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18fc8-128">-WhatIf</span></span>
<span data-ttu-id="18fc8-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18fc8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18fc8-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="18fc8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18fc8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18fc8-131">CommonParameters</span></span>
<span data-ttu-id="18fc8-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18fc8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18fc8-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18fc8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18fc8-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18fc8-134">INPUTS</span></span>

### <span data-ttu-id="18fc8-135">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18fc8-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="18fc8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="18fc8-136">System.String</span></span>

## <span data-ttu-id="18fc8-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18fc8-137">OUTPUTS</span></span>

### <span data-ttu-id="18fc8-138">Microsoft. Azure. Commands. Management. Storage. models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="18fc8-138">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="18fc8-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18fc8-139">NOTES</span></span>

## <span data-ttu-id="18fc8-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18fc8-140">RELATED LINKS</span></span>
