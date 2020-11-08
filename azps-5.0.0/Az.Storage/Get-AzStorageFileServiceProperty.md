---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225314"
---
# <span data-ttu-id="47cd2-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="47cd2-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="47cd2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="47cd2-103">Pobiera właściwości usługi dla usług plików magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="47cd2-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="47cd2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47cd2-104">SYNTAX</span></span>

### <span data-ttu-id="47cd2-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="47cd2-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47cd2-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="47cd2-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47cd2-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="47cd2-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47cd2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="47cd2-108">DESCRIPTION</span></span>
<span data-ttu-id="47cd2-109">Polecenie cmdlet **Get-AzStorageFileServiceProperty** pobiera właściwości usługi dla usług plików magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="47cd2-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="47cd2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47cd2-110">EXAMPLES</span></span>

### <span data-ttu-id="47cd2-111">Przykład 1: pobieranie właściwości usługi plików magazynu platformy Azure określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="47cd2-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="47cd2-112">To polecenie pobiera właściwość usługi plików określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="47cd2-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="47cd2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47cd2-113">PARAMETERS</span></span>

### <span data-ttu-id="47cd2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47cd2-114">-DefaultProfile</span></span>
<span data-ttu-id="47cd2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47cd2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47cd2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47cd2-116">-ResourceGroupName</span></span>
<span data-ttu-id="47cd2-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47cd2-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="47cd2-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47cd2-118">-ResourceId</span></span>
<span data-ttu-id="47cd2-119">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi plików.</span><span class="sxs-lookup"><span data-stu-id="47cd2-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="47cd2-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="47cd2-120">-StorageAccount</span></span>
<span data-ttu-id="47cd2-121">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="47cd2-121">Storage account object</span></span>

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

### <span data-ttu-id="47cd2-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="47cd2-122">-StorageAccountName</span></span>
<span data-ttu-id="47cd2-123">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="47cd2-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="47cd2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47cd2-124">CommonParameters</span></span>
<span data-ttu-id="47cd2-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47cd2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47cd2-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47cd2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47cd2-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47cd2-127">INPUTS</span></span>

### <span data-ttu-id="47cd2-128">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47cd2-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="47cd2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="47cd2-129">System.String</span></span>

## <span data-ttu-id="47cd2-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47cd2-130">OUTPUTS</span></span>

### <span data-ttu-id="47cd2-131">Microsoft. Azure. Commands. Management. Storage. models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="47cd2-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="47cd2-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47cd2-132">NOTES</span></span>

## <span data-ttu-id="47cd2-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47cd2-133">RELATED LINKS</span></span>
