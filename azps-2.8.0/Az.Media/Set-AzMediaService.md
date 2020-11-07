---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: d035890f6478c0b7fd767f12b8f9a27d4f765837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704861"
---
# <span data-ttu-id="b9bdf-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b9bdf-101">Set-AzMediaService</span></span>

## <span data-ttu-id="b9bdf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="b9bdf-103">Modyfikuje określone właściwości istniejącej usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="b9bdf-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="b9bdf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9bdf-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9bdf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b9bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="b9bdf-106">Polecenie cmdlet **Set-AzMediaService** modyfikuje określone właściwości istniejącej usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="b9bdf-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="b9bdf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9bdf-107">EXAMPLES</span></span>

### <span data-ttu-id="b9bdf-108">Przykład 1: modyfikowanie istniejącej usługi multimedialnej</span><span class="sxs-lookup"><span data-stu-id="b9bdf-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="b9bdf-109">Pierwsze polecenie tworzy serię znaczników i zapisuje te znaczniki w zmiennej o nazwie $Tags.</span><span class="sxs-lookup"><span data-stu-id="b9bdf-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="b9bdf-110">To drugie polecenie powoduje zaktualizowanie usługi multimedialnej o nazwie MediaService001 należącej do grupy zasobów o nazwie ResourceGroup123 ze znacznikami przechowywanymi w zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="b9bdf-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="b9bdf-111">W poleceniu użyto również tablicy obiektów konfiguracji magazynu przechowywanych w zmiennej $StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="b9bdf-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="b9bdf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9bdf-112">PARAMETERS</span></span>

### <span data-ttu-id="b9bdf-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b9bdf-113">-AccountName</span></span>
<span data-ttu-id="b9bdf-114">Określa nazwę usługi multimediów, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="b9bdf-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b9bdf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9bdf-115">-DefaultProfile</span></span>
<span data-ttu-id="b9bdf-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b9bdf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9bdf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9bdf-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9bdf-118">Określa nazwę grupy zasobów zawierającej usługę Media.</span><span class="sxs-lookup"><span data-stu-id="b9bdf-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="b9bdf-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="b9bdf-119">-StorageAccounts</span></span>
<span data-ttu-id="b9bdf-120">Określa tablicę kont magazynu, które to polecenie cmdlet kojarzy z usługą multimediów.</span><span class="sxs-lookup"><span data-stu-id="b9bdf-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="b9bdf-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="b9bdf-121">-Tag</span></span>
<span data-ttu-id="b9bdf-122">Tagi skojarzone z kontem multimedialnym.</span><span class="sxs-lookup"><span data-stu-id="b9bdf-122">The tags associated with the media account.</span></span>

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

### <span data-ttu-id="b9bdf-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9bdf-123">-Confirm</span></span>
<span data-ttu-id="b9bdf-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9bdf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9bdf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9bdf-125">-WhatIf</span></span>
<span data-ttu-id="b9bdf-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9bdf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9bdf-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b9bdf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9bdf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9bdf-128">CommonParameters</span></span>
<span data-ttu-id="b9bdf-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9bdf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9bdf-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9bdf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9bdf-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9bdf-131">INPUTS</span></span>

### <span data-ttu-id="b9bdf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b9bdf-132">System.String</span></span>

### <span data-ttu-id="b9bdf-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b9bdf-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b9bdf-134">Microsoft. Azure. Commands. Media. models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="b9bdf-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="b9bdf-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9bdf-135">OUTPUTS</span></span>

### <span data-ttu-id="b9bdf-136">Microsoft. Azure. Commands. Media. models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="b9bdf-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="b9bdf-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9bdf-137">NOTES</span></span>

## <span data-ttu-id="b9bdf-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9bdf-138">RELATED LINKS</span></span>

[<span data-ttu-id="b9bdf-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b9bdf-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="b9bdf-140">Nowe — AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b9bdf-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="b9bdf-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b9bdf-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


