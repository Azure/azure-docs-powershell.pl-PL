---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
ms.openlocfilehash: 7b8c1b154a631a911100f4b2b8581ca552e4b565
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551844"
---
# <span data-ttu-id="4d522-101">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="4d522-101">Set-AzureRmMediaServiceKey</span></span>

## <span data-ttu-id="4d522-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d522-102">SYNOPSIS</span></span>
<span data-ttu-id="4d522-103">Generuje ponownie klucz służący do uzyskiwania dostępu do punktu końcowego usługi do końca skojarzonego z usługą multimediów.</span><span class="sxs-lookup"><span data-stu-id="4d522-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d522-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d522-104">SYNTAX</span></span>

```
Set-AzureRmMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d522-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d522-105">DESCRIPTION</span></span>
<span data-ttu-id="4d522-106">Polecenie cmdlet **Set-AzureRmMediaServiceKey** generuje klucz służący do uzyskiwania dostępu do punktu końcowego przeniesień stanu do reprezentacji (spoczynku) skojarzonego z usługą multimediów.</span><span class="sxs-lookup"><span data-stu-id="4d522-106">The **Set-AzureRmMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="4d522-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d522-107">EXAMPLES</span></span>

### <span data-ttu-id="4d522-108">Przykład 1. Regeneruj klucz podstawowy służący do uzyskiwania dostępu do usługi multimedialnej</span><span class="sxs-lookup"><span data-stu-id="4d522-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="4d522-109">To polecenie generuje ponownie klucz podstawowy usługi multimedialnej o nazwie MediaService001 należącej do grupy zasobów o nazwie ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="4d522-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="4d522-110">Przykład 2. regeneruje klucz pomocniczy służący do uzyskiwania dostępu do usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="4d522-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="4d522-111">To polecenie generuje ponownie klucz pomocniczy dla usługi multimediów o nazwie MediaService002 należącej do grupy zasobów o nazwie Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="4d522-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="4d522-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d522-112">PARAMETERS</span></span>

### <span data-ttu-id="4d522-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4d522-113">-AccountName</span></span>
<span data-ttu-id="4d522-114">Określa nazwę usługi multimediów, która zostanie ponownie wyodtwarzana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d522-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="4d522-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4d522-115">-KeyType</span></span>
<span data-ttu-id="4d522-116">Określa typ klucza usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="4d522-116">Specifies the key type of the media service.</span></span>
<span data-ttu-id="4d522-117">Dopuszczalne wartości tego parametru to: podstawowy lub pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="4d522-117">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d522-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d522-118">-ResourceGroupName</span></span>
<span data-ttu-id="4d522-119">Określa nazwę grupy zasobów zawierającej usługę Media.</span><span class="sxs-lookup"><span data-stu-id="4d522-119">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="4d522-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d522-120">-Confirm</span></span>
<span data-ttu-id="4d522-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d522-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d522-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d522-122">-WhatIf</span></span>
<span data-ttu-id="4d522-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d522-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d522-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d522-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d522-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d522-125">-DefaultProfile</span></span>
<span data-ttu-id="4d522-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d522-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d522-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d522-127">CommonParameters</span></span>
<span data-ttu-id="4d522-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d522-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d522-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d522-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d522-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d522-130">INPUTS</span></span>

## <span data-ttu-id="4d522-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d522-131">OUTPUTS</span></span>

### <span data-ttu-id="4d522-132">Microsoft. Azure. Commands. Media. models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="4d522-132">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="4d522-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d522-133">NOTES</span></span>

## <span data-ttu-id="4d522-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d522-134">RELATED LINKS</span></span>

[<span data-ttu-id="4d522-135">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="4d522-135">Get-AzureRmMediaServiceKeys</span></span>](./Get-AzureRmMediaServiceKeys.md)


