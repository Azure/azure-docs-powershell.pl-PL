---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 19db06ff5563e954124ab36274d62cce0e51b3a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549968"
---
# <span data-ttu-id="3097c-101">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3097c-101">Set-AzureRmMediaService</span></span>

## <span data-ttu-id="3097c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3097c-102">SYNOPSIS</span></span>
<span data-ttu-id="3097c-103">Modyfikuje określone właściwości istniejącej usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="3097c-103">Modifies specified properties of an existing media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3097c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3097c-104">SYNTAX</span></span>

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tags <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3097c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3097c-105">DESCRIPTION</span></span>
<span data-ttu-id="3097c-106">Polecenie cmdlet **Set-AzureRmMediaService** modyfikuje określone właściwości istniejącej usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="3097c-106">The **Set-AzureRmMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="3097c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3097c-107">EXAMPLES</span></span>

### <span data-ttu-id="3097c-108">Przykład 1: modyfikowanie istniejącej usługi multimedialnej</span><span class="sxs-lookup"><span data-stu-id="3097c-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="3097c-109">Pierwsze polecenie tworzy serię znaczników i zapisuje te znaczniki w zmiennej o nazwie $Tags.</span><span class="sxs-lookup"><span data-stu-id="3097c-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>

<span data-ttu-id="3097c-110">To drugie polecenie powoduje zaktualizowanie usługi multimedialnej o nazwie MediaService001 należącej do grupy zasobów o nazwie ResourceGroup123 ze znacznikami przechowywanymi w zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="3097c-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="3097c-111">W poleceniu użyto również tablicy obiektów konfiguracji magazynu przechowywanych w zmiennej $StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="3097c-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="3097c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3097c-112">PARAMETERS</span></span>

### <span data-ttu-id="3097c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3097c-113">-AccountName</span></span>
<span data-ttu-id="3097c-114">Określa nazwę usługi multimediów, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="3097c-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3097c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3097c-115">-ResourceGroupName</span></span>
<span data-ttu-id="3097c-116">Określa nazwę grupy zasobów zawierającej usługę Media.</span><span class="sxs-lookup"><span data-stu-id="3097c-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="3097c-117">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="3097c-117">-StorageAccounts</span></span>
<span data-ttu-id="3097c-118">Określa tablicę kont magazynu, które to polecenie cmdlet kojarzy z usługą multimediów.</span><span class="sxs-lookup"><span data-stu-id="3097c-118">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="3097c-119">-Tagi</span><span class="sxs-lookup"><span data-stu-id="3097c-119">-Tags</span></span>
<span data-ttu-id="3097c-120">Określa Tagi dla usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="3097c-120">Specifies tags for the media service.</span></span>

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

### <span data-ttu-id="3097c-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3097c-121">-Confirm</span></span>
<span data-ttu-id="3097c-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3097c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3097c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3097c-123">-WhatIf</span></span>
<span data-ttu-id="3097c-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3097c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3097c-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3097c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3097c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3097c-126">-DefaultProfile</span></span>
<span data-ttu-id="3097c-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3097c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3097c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3097c-128">CommonParameters</span></span>
<span data-ttu-id="3097c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3097c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3097c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3097c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3097c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3097c-131">INPUTS</span></span>

## <span data-ttu-id="3097c-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3097c-132">OUTPUTS</span></span>

### <span data-ttu-id="3097c-133">Microsoft. Azure. Commands. Media. models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="3097c-133">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="3097c-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3097c-134">NOTES</span></span>

## <span data-ttu-id="3097c-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3097c-135">RELATED LINKS</span></span>

[<span data-ttu-id="3097c-136">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3097c-136">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="3097c-137">Nowe — AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3097c-137">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="3097c-138">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3097c-138">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)


