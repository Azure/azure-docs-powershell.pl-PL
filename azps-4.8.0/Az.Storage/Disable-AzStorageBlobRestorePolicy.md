---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064675"
---
# <span data-ttu-id="f65c4-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="f65c4-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="f65c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f65c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f65c4-103">Wyłącza zasady przywracania obiektu BLOB na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="f65c4-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="f65c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f65c4-104">SYNTAX</span></span>

### <span data-ttu-id="f65c4-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f65c4-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f65c4-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="f65c4-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f65c4-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="f65c4-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f65c4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f65c4-108">DESCRIPTION</span></span>
<span data-ttu-id="f65c4-109">Polecenie cmdlet **disable-AzStorageBlobRestorePolicy** wyłącza zasady przywracania obiektu BLOB dla usługi Azure Storage BLOB.</span><span class="sxs-lookup"><span data-stu-id="f65c4-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f65c4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f65c4-110">EXAMPLES</span></span>

### <span data-ttu-id="f65c4-111">Przykład 1: wyłącza zasady przywracania obiektu BLOB usługi Azure Storage BLOB na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="f65c4-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="f65c4-112">To polecenie wyłącza zasady przywracania obiektów BLOB usługi Azure Storage w ramach konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f65c4-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="f65c4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f65c4-113">PARAMETERS</span></span>

### <span data-ttu-id="f65c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f65c4-114">-DefaultProfile</span></span>
<span data-ttu-id="f65c4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f65c4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f65c4-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f65c4-116">-PassThru</span></span>
<span data-ttu-id="f65c4-117">Wyświetlanie właściwości serviceproperties</span><span class="sxs-lookup"><span data-stu-id="f65c4-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="f65c4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f65c4-118">-ResourceGroupName</span></span>
<span data-ttu-id="f65c4-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f65c4-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="f65c4-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f65c4-120">-ResourceId</span></span>
<span data-ttu-id="f65c4-121">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="f65c4-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="f65c4-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f65c4-122">-StorageAccount</span></span>
<span data-ttu-id="f65c4-123">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="f65c4-123">Storage account object</span></span>

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

### <span data-ttu-id="f65c4-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f65c4-124">-StorageAccountName</span></span>
<span data-ttu-id="f65c4-125">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f65c4-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="f65c4-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f65c4-126">-Confirm</span></span>
<span data-ttu-id="f65c4-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f65c4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f65c4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f65c4-128">-WhatIf</span></span>
<span data-ttu-id="f65c4-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f65c4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f65c4-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f65c4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f65c4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f65c4-131">CommonParameters</span></span>
<span data-ttu-id="f65c4-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f65c4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f65c4-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f65c4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f65c4-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f65c4-134">INPUTS</span></span>

### <span data-ttu-id="f65c4-135">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f65c4-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f65c4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f65c4-136">System.String</span></span>

## <span data-ttu-id="f65c4-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f65c4-137">OUTPUTS</span></span>

### <span data-ttu-id="f65c4-138">Microsoft. Azure. Commands. Management. Storage. models. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="f65c4-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="f65c4-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f65c4-139">NOTES</span></span>

## <span data-ttu-id="f65c4-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f65c4-140">RELATED LINKS</span></span>
