---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: b086703ba8466c6d67e297002e2127a092175c85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707664"
---
# <span data-ttu-id="81a31-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="81a31-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="81a31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81a31-102">SYNOPSIS</span></span>
<span data-ttu-id="81a31-103">Wyłącz zasadę usuwania zasad przechowywania dla usługi blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="81a31-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="81a31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81a31-104">SYNTAX</span></span>

### <span data-ttu-id="81a31-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="81a31-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81a31-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="81a31-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81a31-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="81a31-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81a31-108">Opis</span><span class="sxs-lookup"><span data-stu-id="81a31-108">DESCRIPTION</span></span>
<span data-ttu-id="81a31-109">Polecenie cmdlet **disable-AzStorageBlobDeleteRetentionPolicy** wyłącza zasady dotyczące przechowywania obiektów BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="81a31-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="81a31-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81a31-110">EXAMPLES</span></span>

### <span data-ttu-id="81a31-111">Przykład 1. Wyłącz zasady usuwania zasad przechowywania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="81a31-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="81a31-112">To polecenie wyłącza zasady usuwania zasad przechowywania dla usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="81a31-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="81a31-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81a31-113">PARAMETERS</span></span>

### <span data-ttu-id="81a31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a31-114">-DefaultProfile</span></span>
<span data-ttu-id="81a31-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81a31-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81a31-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81a31-116">-PassThru</span></span>
<span data-ttu-id="81a31-117">Wyświetlanie właściwości serviceproperties</span><span class="sxs-lookup"><span data-stu-id="81a31-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="81a31-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81a31-118">-ResourceGroupName</span></span>
<span data-ttu-id="81a31-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81a31-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="81a31-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81a31-120">-ResourceId</span></span>
<span data-ttu-id="81a31-121">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="81a31-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="81a31-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="81a31-122">-StorageAccount</span></span>
<span data-ttu-id="81a31-123">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="81a31-123">Storage account object</span></span>

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

### <span data-ttu-id="81a31-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="81a31-124">-StorageAccountName</span></span>
<span data-ttu-id="81a31-125">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="81a31-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="81a31-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81a31-126">-Confirm</span></span>
<span data-ttu-id="81a31-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81a31-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81a31-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81a31-128">-WhatIf</span></span>
<span data-ttu-id="81a31-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81a31-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81a31-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81a31-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81a31-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a31-131">CommonParameters</span></span>
<span data-ttu-id="81a31-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a31-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a31-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a31-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a31-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81a31-134">INPUTS</span></span>

### <span data-ttu-id="81a31-135">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="81a31-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="81a31-136">System. String</span><span class="sxs-lookup"><span data-stu-id="81a31-136">System.String</span></span>

## <span data-ttu-id="81a31-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81a31-137">OUTPUTS</span></span>

### <span data-ttu-id="81a31-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="81a31-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="81a31-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81a31-139">NOTES</span></span>

## <span data-ttu-id="81a31-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81a31-140">RELATED LINKS</span></span>