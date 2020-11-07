---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 9507cc178613a80ff0d49ed62e7e43698f5f1d7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718169"
---
# <span data-ttu-id="aa123-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="aa123-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="aa123-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa123-102">SYNOPSIS</span></span>
<span data-ttu-id="aa123-103">Umożliwia usunięcie usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="aa123-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa123-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa123-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa123-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa123-105">DESCRIPTION</span></span>
<span data-ttu-id="aa123-106">Polecenie cmdlet **Remove-AzureRmMediaService** umożliwia usunięcie usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="aa123-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="aa123-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa123-107">EXAMPLES</span></span>

### <span data-ttu-id="aa123-108">Przykład 1: Usuwanie usługi multimedialnej</span><span class="sxs-lookup"><span data-stu-id="aa123-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="aa123-109">To polecenie powoduje usunięcie usługi multimedialnej o nazwie MediaService0011 w grupie zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="aa123-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="aa123-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa123-110">PARAMETERS</span></span>

### <span data-ttu-id="aa123-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aa123-111">-AccountName</span></span>
<span data-ttu-id="aa123-112">Określa nazwę usługi multimedialnej, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa123-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aa123-113">-Force</span><span class="sxs-lookup"><span data-stu-id="aa123-113">-Force</span></span>
<span data-ttu-id="aa123-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="aa123-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aa123-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa123-115">-ResourceGroupName</span></span>
<span data-ttu-id="aa123-116">Określa nazwę grupy zasobów zawierającej usługę Media.</span><span class="sxs-lookup"><span data-stu-id="aa123-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="aa123-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa123-117">-Confirm</span></span>
<span data-ttu-id="aa123-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa123-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa123-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa123-119">-WhatIf</span></span>
<span data-ttu-id="aa123-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa123-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa123-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa123-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa123-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa123-122">-DefaultProfile</span></span>
<span data-ttu-id="aa123-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa123-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa123-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa123-124">CommonParameters</span></span>
<span data-ttu-id="aa123-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa123-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa123-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa123-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa123-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa123-127">INPUTS</span></span>

## <span data-ttu-id="aa123-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa123-128">OUTPUTS</span></span>

### <span data-ttu-id="aa123-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa123-129">System.Boolean</span></span>

## <span data-ttu-id="aa123-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa123-130">NOTES</span></span>

## <span data-ttu-id="aa123-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa123-131">RELATED LINKS</span></span>

[<span data-ttu-id="aa123-132">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="aa123-132">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="aa123-133">Nowe — AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="aa123-133">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="aa123-134">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="aa123-134">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


