---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: c57f8a7ce6b4f7275e724c777c2e6dfd54a680ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190723"
---
# <span data-ttu-id="73801-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73801-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="73801-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73801-102">SYNOPSIS</span></span>
<span data-ttu-id="73801-103">Modyfikuje bieżące konto magazynu dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="73801-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="73801-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="73801-104">SYNTAX</span></span>

### <span data-ttu-id="73801-105">UsingResourceGroupAndNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="73801-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73801-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="73801-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73801-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="73801-107">DESCRIPTION</span></span>
<span data-ttu-id="73801-108">Polecenie **cmdlet Set-AzCurrentStorageAccount** modyfikuje bieżące konto usługi Azure Storage określonej subskrypcji platformy Azure w programie Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="73801-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="73801-109">Bieżące konto magazynu jest używane jako domyślne podczas uzyskiwania dostępu do magazynu bez określania nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="73801-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="73801-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="73801-110">EXAMPLES</span></span>

### <span data-ttu-id="73801-111">Przykład 1. Ustawianie bieżącego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="73801-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="73801-112">To polecenie ustawia domyślne konto magazynu dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="73801-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="73801-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73801-113">PARAMETERS</span></span>

### <span data-ttu-id="73801-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="73801-114">-Context</span></span>
<span data-ttu-id="73801-115">Określa obiekt **AzureStorageContext** dla bieżącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="73801-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="73801-116">Aby uzyskać obiekt kontekstu magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73801-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="73801-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73801-117">-DefaultProfile</span></span>
<span data-ttu-id="73801-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="73801-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73801-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="73801-119">-Name</span></span>
<span data-ttu-id="73801-120">Określa nazwę konta magazynu, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73801-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="73801-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73801-121">-ResourceGroupName</span></span>
<span data-ttu-id="73801-122">Określa grupę zasobów zawierającą konto magazynu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="73801-122">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="73801-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73801-123">CommonParameters</span></span>
<span data-ttu-id="73801-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73801-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73801-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73801-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73801-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73801-126">INPUTS</span></span>

### <span data-ttu-id="73801-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="73801-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="73801-128">System.String</span><span class="sxs-lookup"><span data-stu-id="73801-128">System.String</span></span>

## <span data-ttu-id="73801-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73801-129">OUTPUTS</span></span>

### <span data-ttu-id="73801-130">System.String</span><span class="sxs-lookup"><span data-stu-id="73801-130">System.String</span></span>

## <span data-ttu-id="73801-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="73801-131">NOTES</span></span>

## <span data-ttu-id="73801-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73801-132">RELATED LINKS</span></span>

[<span data-ttu-id="73801-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73801-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


