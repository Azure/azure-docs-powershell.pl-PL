---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: ba63794844420accf2e5e664a43f74b2578c780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717146"
---
# <span data-ttu-id="e0f10-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e0f10-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="e0f10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0f10-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f10-103">Umożliwia usunięcie konta magazynu z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f10-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0f10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0f10-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0f10-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e0f10-105">DESCRIPTION</span></span>
<span data-ttu-id="e0f10-106">Polecenie cmdlet **Remove-AzureRmStorageAccount** umożliwia usunięcie konta magazynu z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f10-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="e0f10-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0f10-107">EXAMPLES</span></span>

### <span data-ttu-id="e0f10-108">Przykład 1: usuwanie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="e0f10-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="e0f10-109">To polecenie umożliwia usunięcie określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e0f10-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="e0f10-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0f10-110">PARAMETERS</span></span>

### <span data-ttu-id="e0f10-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e0f10-111">-Force</span></span>
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

### <span data-ttu-id="e0f10-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e0f10-112">-Name</span></span>
<span data-ttu-id="e0f10-113">Określa nazwę konta magazynu, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="e0f10-113">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="e0f10-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0f10-114">-ResourceGroupName</span></span>
<span data-ttu-id="e0f10-115">Określa nazwę grupy zasobów zawierającej konto magazynu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e0f10-115">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="e0f10-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0f10-116">-Confirm</span></span>
<span data-ttu-id="e0f10-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0f10-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f10-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0f10-118">-WhatIf</span></span>
<span data-ttu-id="e0f10-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0f10-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0f10-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e0f10-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f10-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f10-121">-DefaultProfile</span></span>
<span data-ttu-id="e0f10-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f10-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0f10-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f10-123">CommonParameters</span></span>
<span data-ttu-id="e0f10-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0f10-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f10-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0f10-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f10-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0f10-126">INPUTS</span></span>

## <span data-ttu-id="e0f10-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0f10-127">OUTPUTS</span></span>

## <span data-ttu-id="e0f10-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0f10-128">NOTES</span></span>

## <span data-ttu-id="e0f10-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0f10-129">RELATED LINKS</span></span>

[<span data-ttu-id="e0f10-130">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e0f10-130">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="e0f10-131">Nowe — AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e0f10-131">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="e0f10-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e0f10-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


