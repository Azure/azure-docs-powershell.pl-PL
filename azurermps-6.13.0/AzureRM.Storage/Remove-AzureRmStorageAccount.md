---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: 9c512c1993700e1bbdab4d5c0d52a1aa2ceeafb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553412"
---
# <span data-ttu-id="01692-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01692-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="01692-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01692-102">SYNOPSIS</span></span>
<span data-ttu-id="01692-103">Umożliwia usunięcie konta magazynu z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="01692-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01692-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01692-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01692-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01692-105">DESCRIPTION</span></span>
<span data-ttu-id="01692-106">Polecenie cmdlet **Remove-AzureRmStorageAccount** umożliwia usunięcie konta magazynu z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="01692-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="01692-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01692-107">EXAMPLES</span></span>

### <span data-ttu-id="01692-108">Przykład 1: usuwanie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="01692-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="01692-109">To polecenie umożliwia usunięcie określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="01692-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="01692-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01692-110">PARAMETERS</span></span>

### <span data-ttu-id="01692-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01692-111">-AsJob</span></span>
<span data-ttu-id="01692-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="01692-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01692-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01692-113">-DefaultProfile</span></span>
<span data-ttu-id="01692-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01692-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01692-115">-Force</span><span class="sxs-lookup"><span data-stu-id="01692-115">-Force</span></span>
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

### <span data-ttu-id="01692-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="01692-116">-Name</span></span>
<span data-ttu-id="01692-117">Określa nazwę konta magazynu, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="01692-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="01692-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01692-118">-ResourceGroupName</span></span>
<span data-ttu-id="01692-119">Określa nazwę grupy zasobów zawierającej konto magazynu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="01692-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="01692-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01692-120">-Confirm</span></span>
<span data-ttu-id="01692-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01692-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01692-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01692-122">-WhatIf</span></span>
<span data-ttu-id="01692-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01692-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01692-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="01692-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01692-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01692-125">CommonParameters</span></span>
<span data-ttu-id="01692-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01692-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01692-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01692-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01692-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01692-128">INPUTS</span></span>

### <span data-ttu-id="01692-129">System. String</span><span class="sxs-lookup"><span data-stu-id="01692-129">System.String</span></span>

## <span data-ttu-id="01692-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01692-130">OUTPUTS</span></span>

### <span data-ttu-id="01692-131">System. void</span><span class="sxs-lookup"><span data-stu-id="01692-131">System.Void</span></span>

## <span data-ttu-id="01692-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01692-132">NOTES</span></span>

## <span data-ttu-id="01692-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01692-133">RELATED LINKS</span></span>

[<span data-ttu-id="01692-134">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01692-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="01692-135">Nowe — AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01692-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="01692-136">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01692-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


