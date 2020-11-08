---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 44c1ff2fe283e3cd804d20a8df21023b3c222150
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233354"
---
# <span data-ttu-id="79124-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="79124-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="79124-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79124-102">SYNOPSIS</span></span>
<span data-ttu-id="79124-103">Generuje ponownie klucz służący do uzyskiwania dostępu do punktu końcowego usługi do końca skojarzonego z usługą multimediów.</span><span class="sxs-lookup"><span data-stu-id="79124-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="79124-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79124-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79124-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79124-105">DESCRIPTION</span></span>
<span data-ttu-id="79124-106">Polecenie cmdlet **Set-AzMediaServiceKey** generuje klucz służący do uzyskiwania dostępu do punktu końcowego przeniesień stanu do reprezentacji (spoczynku) skojarzonego z usługą multimediów.</span><span class="sxs-lookup"><span data-stu-id="79124-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="79124-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79124-107">EXAMPLES</span></span>

### <span data-ttu-id="79124-108">Przykład 1. Regeneruj klucz podstawowy służący do uzyskiwania dostępu do usługi multimedialnej</span><span class="sxs-lookup"><span data-stu-id="79124-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="79124-109">To polecenie generuje ponownie klucz podstawowy usługi multimedialnej o nazwie MediaService001 należącej do grupy zasobów o nazwie ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="79124-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="79124-110">Przykład 2. regeneruje klucz pomocniczy służący do uzyskiwania dostępu do usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="79124-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="79124-111">To polecenie generuje ponownie klucz pomocniczy dla usługi multimediów o nazwie MediaService002 należącej do grupy zasobów o nazwie Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="79124-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="79124-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79124-112">PARAMETERS</span></span>

### <span data-ttu-id="79124-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79124-113">-AccountName</span></span>
<span data-ttu-id="79124-114">Określa nazwę usługi multimediów, która zostanie ponownie wyodtwarzana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79124-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="79124-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79124-115">-DefaultProfile</span></span>
<span data-ttu-id="79124-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="79124-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79124-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="79124-117">-KeyType</span></span>
<span data-ttu-id="79124-118">Określa typ klucza usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="79124-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="79124-119">Dopuszczalne wartości tego parametru to: podstawowy lub pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="79124-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="79124-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79124-120">-ResourceGroupName</span></span>
<span data-ttu-id="79124-121">Określa nazwę grupy zasobów zawierającej usługę Media.</span><span class="sxs-lookup"><span data-stu-id="79124-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="79124-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79124-122">-Confirm</span></span>
<span data-ttu-id="79124-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79124-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79124-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79124-124">-WhatIf</span></span>
<span data-ttu-id="79124-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79124-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79124-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79124-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79124-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79124-127">CommonParameters</span></span>
<span data-ttu-id="79124-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79124-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79124-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79124-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79124-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79124-130">INPUTS</span></span>

### <span data-ttu-id="79124-131">System. String</span><span class="sxs-lookup"><span data-stu-id="79124-131">System.String</span></span>

## <span data-ttu-id="79124-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79124-132">OUTPUTS</span></span>

### <span data-ttu-id="79124-133">Microsoft. Azure. Commands. Media. models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="79124-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="79124-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79124-134">NOTES</span></span>

## <span data-ttu-id="79124-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79124-135">RELATED LINKS</span></span>

[<span data-ttu-id="79124-136">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="79124-136">Get-AzMediaServiceKey</span></span>](./Get-AzMediaServiceKey.md)


