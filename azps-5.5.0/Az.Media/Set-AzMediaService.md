---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: 5b85e3e64b4a79b33975d9b29d0498ac8ae0ce03
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203615"
---
# <span data-ttu-id="577ec-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="577ec-101">Set-AzMediaService</span></span>

## <span data-ttu-id="577ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="577ec-102">SYNOPSIS</span></span>
<span data-ttu-id="577ec-103">Modyfikuje określone właściwości istniejącej usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="577ec-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="577ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="577ec-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="577ec-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="577ec-105">DESCRIPTION</span></span>
<span data-ttu-id="577ec-106">Polecenie **cmdlet Set-AzMediaService** modyfikuje określone właściwości istniejącej usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="577ec-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="577ec-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="577ec-107">EXAMPLES</span></span>

### <span data-ttu-id="577ec-108">Przykład 1. Modyfikowanie istniejącej usługi multimediów</span><span class="sxs-lookup"><span data-stu-id="577ec-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="577ec-109">Pierwsze polecenie tworzy serię tagów i przechowuje je w zmiennej o nazwie $Tags.</span><span class="sxs-lookup"><span data-stu-id="577ec-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="577ec-110">Drugie polecenie aktualizuje usługę multimediów o nazwie MediaService001, która należy do grupy zasobów o nazwie ResourceGroup123, przy użyciu tagów przechowywanych w $Tags zmienną.</span><span class="sxs-lookup"><span data-stu-id="577ec-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="577ec-111">To polecenie korzysta również z tablicy obiektów konfiguracji magazynu przechowywanych w $StorageAccounts danych.</span><span class="sxs-lookup"><span data-stu-id="577ec-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="577ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="577ec-112">PARAMETERS</span></span>

### <span data-ttu-id="577ec-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="577ec-113">-AccountName</span></span>
<span data-ttu-id="577ec-114">Określa nazwę usługi multimediów, która ma być zmieniana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="577ec-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="577ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577ec-115">-DefaultProfile</span></span>
<span data-ttu-id="577ec-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="577ec-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="577ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="577ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="577ec-118">Określa nazwę grupy zasobów zawierającej usługę multimediów.</span><span class="sxs-lookup"><span data-stu-id="577ec-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="577ec-119">— StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="577ec-119">-StorageAccounts</span></span>
<span data-ttu-id="577ec-120">Określa tablicę kont magazynu, które to polecenie cmdlet skojarzy z usługą multimediów.</span><span class="sxs-lookup"><span data-stu-id="577ec-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="577ec-121">— Tag</span><span class="sxs-lookup"><span data-stu-id="577ec-121">-Tag</span></span>
<span data-ttu-id="577ec-122">Tagi skojarzone z kontem multimedialnym.</span><span class="sxs-lookup"><span data-stu-id="577ec-122">The tags associated with the media account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="577ec-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="577ec-123">-Confirm</span></span>
<span data-ttu-id="577ec-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="577ec-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="577ec-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="577ec-125">-WhatIf</span></span>
<span data-ttu-id="577ec-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="577ec-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="577ec-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="577ec-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="577ec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577ec-128">CommonParameters</span></span>
<span data-ttu-id="577ec-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="577ec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577ec-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="577ec-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577ec-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="577ec-131">INPUTS</span></span>

### <span data-ttu-id="577ec-132">System.String</span><span class="sxs-lookup"><span data-stu-id="577ec-132">System.String</span></span>

### <span data-ttu-id="577ec-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="577ec-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="577ec-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="577ec-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="577ec-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="577ec-135">OUTPUTS</span></span>

### <span data-ttu-id="577ec-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="577ec-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="577ec-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="577ec-137">NOTES</span></span>

## <span data-ttu-id="577ec-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="577ec-138">RELATED LINKS</span></span>

[<span data-ttu-id="577ec-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="577ec-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="577ec-140">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="577ec-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="577ec-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="577ec-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


