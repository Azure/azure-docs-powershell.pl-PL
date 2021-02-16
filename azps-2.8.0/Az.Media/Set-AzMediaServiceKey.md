---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: c80c9b411d360de0b46cd051a3f786bb740b26f2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411810"
---
# <span data-ttu-id="d61d1-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="d61d1-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="d61d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d61d1-102">SYNOPSIS</span></span>
<span data-ttu-id="d61d1-103">Ponownie generuje klucz używany do uzyskiwania dostępu do punktu końcowego REST skojarzonego z usługą multimediów.</span><span class="sxs-lookup"><span data-stu-id="d61d1-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="d61d1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d61d1-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d61d1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d61d1-105">DESCRIPTION</span></span>
<span data-ttu-id="d61d1-106">Polecenie **cmdlet Set-AzMediaServiceKey** ponownie generuje klucz używany do uzyskiwania dostępu do punktu końcowego REST (Representational State Transfer) skojarzonego z usługą multimedialną.</span><span class="sxs-lookup"><span data-stu-id="d61d1-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="d61d1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d61d1-107">EXAMPLES</span></span>

### <span data-ttu-id="d61d1-108">Przykład 1. Ponowne generowanie klucza podstawowego używanego do uzyskiwania dostępu do usługi multimediów</span><span class="sxs-lookup"><span data-stu-id="d61d1-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="d61d1-109">To polecenie ponownie generuje klucz podstawowy usługi multimediów o nazwie MediaService001, która należy do grupy zasobów o nazwie ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="d61d1-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="d61d1-110">Przykład 2. Ponowne generowanie klucza pomocniczego używanego do uzyskiwania dostępu do usługi multimediów</span><span class="sxs-lookup"><span data-stu-id="d61d1-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="d61d1-111">To polecenie ponownie generuje klucz pomocniczy dla usługi multimediów o nazwie MediaService002, która należy do grupy zasobów o nazwie Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="d61d1-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="d61d1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d61d1-112">PARAMETERS</span></span>

### <span data-ttu-id="d61d1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d61d1-113">-AccountName</span></span>
<span data-ttu-id="d61d1-114">Określa nazwę usługi multimediów, która będzie ponownie generowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d61d1-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="d61d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d61d1-115">-DefaultProfile</span></span>
<span data-ttu-id="d61d1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d61d1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d61d1-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="d61d1-117">-KeyType</span></span>
<span data-ttu-id="d61d1-118">Określa typ klucza usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="d61d1-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="d61d1-119">Dopuszczalne wartości dla tego parametru to: Podstawowy lub Pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="d61d1-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="d61d1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d61d1-120">-ResourceGroupName</span></span>
<span data-ttu-id="d61d1-121">Określa nazwę grupy zasobów zawierającej usługę multimediów.</span><span class="sxs-lookup"><span data-stu-id="d61d1-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="d61d1-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d61d1-122">-Confirm</span></span>
<span data-ttu-id="d61d1-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d61d1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d61d1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d61d1-124">-WhatIf</span></span>
<span data-ttu-id="d61d1-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d61d1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d61d1-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d61d1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d61d1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d61d1-127">CommonParameters</span></span>
<span data-ttu-id="d61d1-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d61d1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d61d1-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d61d1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d61d1-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d61d1-130">INPUTS</span></span>

### <span data-ttu-id="d61d1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d61d1-131">System.String</span></span>

## <span data-ttu-id="d61d1-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d61d1-132">OUTPUTS</span></span>

### <span data-ttu-id="d61d1-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="d61d1-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="d61d1-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d61d1-134">NOTES</span></span>

## <span data-ttu-id="d61d1-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d61d1-135">RELATED LINKS</span></span>



