---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349846"
---
# <span data-ttu-id="c587f-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="c587f-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="c587f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c587f-102">SYNOPSIS</span></span>
<span data-ttu-id="c587f-103">Wyłącza zasady przywracania obiektu BLOB na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="c587f-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="c587f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c587f-104">SYNTAX</span></span>

### <span data-ttu-id="c587f-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c587f-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c587f-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="c587f-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c587f-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="c587f-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c587f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c587f-108">DESCRIPTION</span></span>
<span data-ttu-id="c587f-109">Polecenie cmdlet **disable-AzStorageBlobRestorePolicy** wyłącza zasady przywracania obiektu BLOB dla usługi Azure Storage BLOB.</span><span class="sxs-lookup"><span data-stu-id="c587f-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c587f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c587f-110">EXAMPLES</span></span>

### <span data-ttu-id="c587f-111">Przykład 1: wyłącza zasady przywracania obiektu BLOB usługi Azure Storage BLOB na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="c587f-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="c587f-112">To polecenie wyłącza zasady przywracania obiektów BLOB usługi Azure Storage w ramach konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c587f-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="c587f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c587f-113">PARAMETERS</span></span>

### <span data-ttu-id="c587f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c587f-114">-DefaultProfile</span></span>
<span data-ttu-id="c587f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c587f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c587f-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c587f-116">-PassThru</span></span>
<span data-ttu-id="c587f-117">Wyświetlanie właściwości serviceproperties</span><span class="sxs-lookup"><span data-stu-id="c587f-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="c587f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c587f-118">-ResourceGroupName</span></span>
<span data-ttu-id="c587f-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c587f-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="c587f-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c587f-120">-ResourceId</span></span>
<span data-ttu-id="c587f-121">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="c587f-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="c587f-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c587f-122">-StorageAccount</span></span>
<span data-ttu-id="c587f-123">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c587f-123">Storage account object</span></span>

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

### <span data-ttu-id="c587f-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c587f-124">-StorageAccountName</span></span>
<span data-ttu-id="c587f-125">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c587f-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="c587f-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c587f-126">-Confirm</span></span>
<span data-ttu-id="c587f-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c587f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c587f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c587f-128">-WhatIf</span></span>
<span data-ttu-id="c587f-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c587f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c587f-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c587f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c587f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c587f-131">CommonParameters</span></span>
<span data-ttu-id="c587f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c587f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c587f-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c587f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c587f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c587f-134">INPUTS</span></span>

### <span data-ttu-id="c587f-135">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c587f-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c587f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c587f-136">System.String</span></span>

## <span data-ttu-id="c587f-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c587f-137">OUTPUTS</span></span>

### <span data-ttu-id="c587f-138">Microsoft. Azure. Commands. Management. Storage. models. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="c587f-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="c587f-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c587f-139">NOTES</span></span>

## <span data-ttu-id="c587f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c587f-140">RELATED LINKS</span></span>
