---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: fadeb5c9fdee8028364f8e65ccd7e7e70a20572b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707551"
---
# <span data-ttu-id="26abf-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26abf-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="26abf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26abf-102">SYNOPSIS</span></span>
<span data-ttu-id="26abf-103">Umożliwia usunięcie konta magazynu z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="26abf-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="26abf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26abf-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26abf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="26abf-105">DESCRIPTION</span></span>
<span data-ttu-id="26abf-106">Polecenie cmdlet **Remove-AzStorageAccount** umożliwia usunięcie konta magazynu z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="26abf-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="26abf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26abf-107">EXAMPLES</span></span>

### <span data-ttu-id="26abf-108">Przykład 1: usuwanie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="26abf-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="26abf-109">To polecenie umożliwia usunięcie określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="26abf-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="26abf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26abf-110">PARAMETERS</span></span>

### <span data-ttu-id="26abf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26abf-111">-AsJob</span></span>
<span data-ttu-id="26abf-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="26abf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26abf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26abf-113">-DefaultProfile</span></span>
<span data-ttu-id="26abf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26abf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26abf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="26abf-115">-Force</span></span>
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

### <span data-ttu-id="26abf-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26abf-116">-Name</span></span>
<span data-ttu-id="26abf-117">Określa nazwę konta magazynu, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="26abf-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="26abf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26abf-118">-ResourceGroupName</span></span>
<span data-ttu-id="26abf-119">Określa nazwę grupy zasobów zawierającej konto magazynu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="26abf-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="26abf-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26abf-120">-Confirm</span></span>
<span data-ttu-id="26abf-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26abf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26abf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26abf-122">-WhatIf</span></span>
<span data-ttu-id="26abf-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26abf-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26abf-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26abf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26abf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26abf-125">CommonParameters</span></span>
<span data-ttu-id="26abf-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26abf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26abf-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26abf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26abf-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26abf-128">INPUTS</span></span>

### <span data-ttu-id="26abf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="26abf-129">System.String</span></span>

## <span data-ttu-id="26abf-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26abf-130">OUTPUTS</span></span>

### <span data-ttu-id="26abf-131">System. void</span><span class="sxs-lookup"><span data-stu-id="26abf-131">System.Void</span></span>

## <span data-ttu-id="26abf-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26abf-132">NOTES</span></span>

## <span data-ttu-id="26abf-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26abf-133">RELATED LINKS</span></span>

[<span data-ttu-id="26abf-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26abf-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="26abf-135">Nowe — AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26abf-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="26abf-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26abf-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


