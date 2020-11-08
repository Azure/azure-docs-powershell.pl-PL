---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: faecfdf62892faba2f7ec1241d7e02daa1e6ed12
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051266"
---
# <span data-ttu-id="5a2f9-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5a2f9-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="5a2f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a2f9-102">SYNOPSIS</span></span>
<span data-ttu-id="5a2f9-103">Pobiera klucze dostępu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5a2f9-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="5a2f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a2f9-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a2f9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5a2f9-105">DESCRIPTION</span></span>
<span data-ttu-id="5a2f9-106">Polecenie cmdlet **Get-AzStorageAccountKey** pobiera klucze dostępu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5a2f9-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="5a2f9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a2f9-107">EXAMPLES</span></span>

### <span data-ttu-id="5a2f9-108">Przykład 1: uzyskiwanie klawiszy dostępu dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="5a2f9-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="5a2f9-109">To polecenie pobiera klucze określonego konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5a2f9-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="5a2f9-110">Przykład 2: uzyskiwanie określonego klucza dostępu dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="5a2f9-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

## <span data-ttu-id="5a2f9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a2f9-111">PARAMETERS</span></span>

### <span data-ttu-id="5a2f9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a2f9-112">-DefaultProfile</span></span>
<span data-ttu-id="5a2f9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a2f9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a2f9-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5a2f9-114">-Name</span></span>
<span data-ttu-id="5a2f9-115">Określa nazwę konta magazynu, dla którego to polecenie cmdlet pobiera klucze.</span><span class="sxs-lookup"><span data-stu-id="5a2f9-115">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a2f9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a2f9-116">-ResourceGroupName</span></span>
<span data-ttu-id="5a2f9-117">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="5a2f9-117">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a2f9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a2f9-118">CommonParameters</span></span>
<span data-ttu-id="5a2f9-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a2f9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a2f9-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a2f9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a2f9-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a2f9-121">INPUTS</span></span>

### <span data-ttu-id="5a2f9-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5a2f9-122">System.String</span></span>

## <span data-ttu-id="5a2f9-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a2f9-123">OUTPUTS</span></span>

### <span data-ttu-id="5a2f9-124">Microsoft. Azure. Management. Storage. MODELES. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5a2f9-124">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="5a2f9-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a2f9-125">NOTES</span></span>

## <span data-ttu-id="5a2f9-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a2f9-126">RELATED LINKS</span></span>

[<span data-ttu-id="5a2f9-127">Nowe — AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5a2f9-127">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


