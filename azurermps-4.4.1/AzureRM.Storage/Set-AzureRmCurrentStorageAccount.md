---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
ms.openlocfilehash: 73680e82a9d898075e905d88bcc8602609a5612d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717143"
---
# <span data-ttu-id="ba685-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba685-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="ba685-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba685-102">SYNOPSIS</span></span>
<span data-ttu-id="ba685-103">Modyfikuje bieżące konto magazynu określonego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="ba685-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba685-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba685-104">SYNTAX</span></span>

### <span data-ttu-id="ba685-105">UsingResourceGroupAndNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ba685-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba685-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="ba685-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba685-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ba685-107">DESCRIPTION</span></span>
<span data-ttu-id="ba685-108">Polecenie cmdlet **Set-AzureRmCurrentStorageAccount** modyfikuje bieżące konto magazynu platformy Azure określonej subskrypcji platformy Azure w programie Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ba685-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="ba685-109">Bieżące konto magazynu jest używane jako domyślne podczas uzyskiwania dostępu do magazynu bez określenia nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ba685-109">The current storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="ba685-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba685-110">EXAMPLES</span></span>

### <span data-ttu-id="ba685-111">Przykład 1: Ustawianie bieżącego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="ba685-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="ba685-112">To polecenie ustawia domyślne konto magazynu dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ba685-112">This command sets the default storage account for the specified subscription.</span></span>

## <span data-ttu-id="ba685-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba685-113">PARAMETERS</span></span>

### <span data-ttu-id="ba685-114">-Context</span><span class="sxs-lookup"><span data-stu-id="ba685-114">-Context</span></span>
<span data-ttu-id="ba685-115">Określa obiekt **AzureStorageContext** dla bieżącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ba685-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="ba685-116">Aby uzyskać obiekt kontekstu przechowywania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ba685-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UsingStorageContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba685-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ba685-117">-Name</span></span>
<span data-ttu-id="ba685-118">Określa nazwę konta magazynu, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba685-118">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba685-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba685-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba685-120">Określa grupę zasobów zawierającą konto magazynu, które należy zmodyfikować.</span><span class="sxs-lookup"><span data-stu-id="ba685-120">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba685-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba685-121">-DefaultProfile</span></span>
<span data-ttu-id="ba685-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba685-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba685-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba685-123">CommonParameters</span></span>
<span data-ttu-id="ba685-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba685-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba685-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba685-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba685-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba685-126">INPUTS</span></span>

## <span data-ttu-id="ba685-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba685-127">OUTPUTS</span></span>

## <span data-ttu-id="ba685-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba685-128">NOTES</span></span>

## <span data-ttu-id="ba685-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba685-129">RELATED LINKS</span></span>

[<span data-ttu-id="ba685-130">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba685-130">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


