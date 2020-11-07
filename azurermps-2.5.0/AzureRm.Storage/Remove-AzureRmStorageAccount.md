---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: d3e7a04f292be8e83bc28456c0510450c078a777
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899180"
---
# <span data-ttu-id="b5e02-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5e02-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="b5e02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5e02-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e02-103">Umożliwia usunięcie konta magazynu z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5e02-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5e02-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5e02-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5e02-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5e02-105">DESCRIPTION</span></span>
<span data-ttu-id="b5e02-106">Polecenie cmdlet **Remove-AzureRmStorageAccount** umożliwia usunięcie konta magazynu z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5e02-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="b5e02-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5e02-107">EXAMPLES</span></span>

### <span data-ttu-id="b5e02-108">Przykład 1: usuwanie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b5e02-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="b5e02-109">To polecenie umożliwia usunięcie określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b5e02-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="b5e02-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5e02-110">PARAMETERS</span></span>

### <span data-ttu-id="b5e02-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5e02-111">-AsJob</span></span>
<span data-ttu-id="b5e02-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b5e02-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5e02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e02-113">-DefaultProfile</span></span>
<span data-ttu-id="b5e02-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5e02-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5e02-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b5e02-115">-Force</span></span>
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

### <span data-ttu-id="b5e02-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5e02-116">-Name</span></span>
<span data-ttu-id="b5e02-117">Określa nazwę konta magazynu, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="b5e02-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="b5e02-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5e02-118">-ResourceGroupName</span></span>
<span data-ttu-id="b5e02-119">Określa nazwę grupy zasobów zawierającej konto magazynu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b5e02-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="b5e02-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5e02-120">-Confirm</span></span>
<span data-ttu-id="b5e02-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5e02-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5e02-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5e02-122">-WhatIf</span></span>
<span data-ttu-id="b5e02-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5e02-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5e02-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5e02-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5e02-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e02-125">CommonParameters</span></span>
<span data-ttu-id="b5e02-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5e02-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e02-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5e02-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e02-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5e02-128">INPUTS</span></span>

### <span data-ttu-id="b5e02-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b5e02-129">System.String</span></span>

## <span data-ttu-id="b5e02-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5e02-130">OUTPUTS</span></span>

### <span data-ttu-id="b5e02-131">System. void</span><span class="sxs-lookup"><span data-stu-id="b5e02-131">System.Void</span></span>

## <span data-ttu-id="b5e02-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5e02-132">NOTES</span></span>

## <span data-ttu-id="b5e02-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5e02-133">RELATED LINKS</span></span>

[<span data-ttu-id="b5e02-134">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5e02-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="b5e02-135">Nowe — AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5e02-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="b5e02-136">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5e02-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


