---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: e92bdaae728031ba38fc1326ac2abb29aac86c59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190778"
---
# <span data-ttu-id="d9d07-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9d07-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="d9d07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9d07-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d07-103">Usuwa konto magazynu z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d07-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="d9d07-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9d07-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9d07-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9d07-105">DESCRIPTION</span></span>
<span data-ttu-id="d9d07-106">Polecenie **cmdlet Remove-AzStorageAccount** usuwa konto magazynu z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d07-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="d9d07-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9d07-107">EXAMPLES</span></span>

### <span data-ttu-id="d9d07-108">Przykład 1. Usuwanie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d9d07-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="d9d07-109">To polecenie usuwa określone konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="d9d07-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="d9d07-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9d07-110">PARAMETERS</span></span>

### <span data-ttu-id="d9d07-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d9d07-111">-AsJob</span></span>
<span data-ttu-id="d9d07-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d9d07-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9d07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d07-113">-DefaultProfile</span></span>
<span data-ttu-id="d9d07-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d07-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9d07-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d9d07-115">-Force</span></span>
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

### <span data-ttu-id="d9d07-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d9d07-116">-Name</span></span>
<span data-ttu-id="d9d07-117">Określa nazwę konta magazynu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d9d07-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="d9d07-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9d07-118">-ResourceGroupName</span></span>
<span data-ttu-id="d9d07-119">Określa nazwę grupy zasobów zawierającej konto magazynu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d9d07-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="d9d07-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9d07-120">-Confirm</span></span>
<span data-ttu-id="d9d07-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9d07-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9d07-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9d07-122">-WhatIf</span></span>
<span data-ttu-id="d9d07-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9d07-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9d07-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d9d07-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9d07-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d07-125">CommonParameters</span></span>
<span data-ttu-id="d9d07-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9d07-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d07-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9d07-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d07-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9d07-128">INPUTS</span></span>

### <span data-ttu-id="d9d07-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d9d07-129">System.String</span></span>

## <span data-ttu-id="d9d07-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d9d07-130">OUTPUTS</span></span>

### <span data-ttu-id="d9d07-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="d9d07-131">System.Void</span></span>

## <span data-ttu-id="d9d07-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9d07-132">NOTES</span></span>

## <span data-ttu-id="d9d07-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9d07-133">RELATED LINKS</span></span>

[<span data-ttu-id="d9d07-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9d07-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="d9d07-135">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9d07-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="d9d07-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9d07-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


