---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324973"
---
# <span data-ttu-id="c6f92-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c6f92-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="c6f92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6f92-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f92-103">Pobiera właściwości usługi dla usług plików magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6f92-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="c6f92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6f92-104">SYNTAX</span></span>

### <span data-ttu-id="c6f92-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c6f92-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f92-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="c6f92-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6f92-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="c6f92-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6f92-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c6f92-108">DESCRIPTION</span></span>
<span data-ttu-id="c6f92-109">Polecenie cmdlet **Get-AzStorageFileServiceProperty** pobiera właściwości usługi dla usług plików magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6f92-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="c6f92-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6f92-110">EXAMPLES</span></span>

### <span data-ttu-id="c6f92-111">Przykład 1: pobieranie właściwości usługi plików magazynu platformy Azure określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c6f92-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="c6f92-112">To polecenie pobiera właściwość usługi plików określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6f92-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="c6f92-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6f92-113">PARAMETERS</span></span>

### <span data-ttu-id="c6f92-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f92-114">-DefaultProfile</span></span>
<span data-ttu-id="c6f92-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6f92-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6f92-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6f92-116">-ResourceGroupName</span></span>
<span data-ttu-id="c6f92-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6f92-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="c6f92-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6f92-118">-ResourceId</span></span>
<span data-ttu-id="c6f92-119">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi plików.</span><span class="sxs-lookup"><span data-stu-id="c6f92-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="c6f92-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6f92-120">-StorageAccount</span></span>
<span data-ttu-id="c6f92-121">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c6f92-121">Storage account object</span></span>

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

### <span data-ttu-id="c6f92-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c6f92-122">-StorageAccountName</span></span>
<span data-ttu-id="c6f92-123">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6f92-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="c6f92-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f92-124">CommonParameters</span></span>
<span data-ttu-id="c6f92-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6f92-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f92-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6f92-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f92-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6f92-127">INPUTS</span></span>

### <span data-ttu-id="c6f92-128">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6f92-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c6f92-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c6f92-129">System.String</span></span>

## <span data-ttu-id="c6f92-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6f92-130">OUTPUTS</span></span>

### <span data-ttu-id="c6f92-131">Microsoft. Azure. Commands. Management. Storage. models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="c6f92-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="c6f92-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6f92-132">NOTES</span></span>

## <span data-ttu-id="c6f92-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6f92-133">RELATED LINKS</span></span>
