---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: aeda6548526c4ad12746ce90f1a030f85a0a8d2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950785"
---
# <span data-ttu-id="db3f4-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db3f4-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="db3f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="db3f4-103">Modyfikuje bieżące konto magazynu dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="db3f4-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="db3f4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="db3f4-104">SYNTAX</span></span>

### <span data-ttu-id="db3f4-105">UsingResourceGroupAndNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="db3f4-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db3f4-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="db3f4-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db3f4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="db3f4-107">DESCRIPTION</span></span>
<span data-ttu-id="db3f4-108">Polecenie **cmdlet Set-AzCurrentStorageAccount** modyfikuje bieżące konto usługi Azure Storage określonej subskrypcji platformy Azure w programie Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="db3f4-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="db3f4-109">Bieżące konto magazynu jest używane jako domyślne podczas uzyskiwania dostępu do magazynu bez określania nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="db3f4-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="db3f4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="db3f4-110">EXAMPLES</span></span>

### <span data-ttu-id="db3f4-111">Przykład 1. Ustawianie bieżącego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="db3f4-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="db3f4-112">To polecenie ustawia domyślne konto magazynu dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="db3f4-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="db3f4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db3f4-113">PARAMETERS</span></span>

### <span data-ttu-id="db3f4-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="db3f4-114">-Context</span></span>
<span data-ttu-id="db3f4-115">Określa obiekt **AzureStorageContext** dla bieżącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="db3f4-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="db3f4-116">Aby uzyskać obiekt kontekstu magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db3f4-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="db3f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db3f4-117">-DefaultProfile</span></span>
<span data-ttu-id="db3f4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="db3f4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db3f4-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="db3f4-119">-Name</span></span>
<span data-ttu-id="db3f4-120">Określa nazwę konta magazynu, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db3f4-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="db3f4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db3f4-121">-ResourceGroupName</span></span>
<span data-ttu-id="db3f4-122">Określa grupę zasobów zawierającą konto magazynu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="db3f4-122">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="db3f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db3f4-123">CommonParameters</span></span>
<span data-ttu-id="db3f4-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db3f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db3f4-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db3f4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db3f4-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db3f4-126">INPUTS</span></span>

### <span data-ttu-id="db3f4-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="db3f4-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="db3f4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="db3f4-128">System.String</span></span>

## <span data-ttu-id="db3f4-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db3f4-129">OUTPUTS</span></span>

### <span data-ttu-id="db3f4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="db3f4-130">System.String</span></span>

## <span data-ttu-id="db3f4-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="db3f4-131">NOTES</span></span>

## <span data-ttu-id="db3f4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db3f4-132">RELATED LINKS</span></span>

[<span data-ttu-id="db3f4-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db3f4-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


