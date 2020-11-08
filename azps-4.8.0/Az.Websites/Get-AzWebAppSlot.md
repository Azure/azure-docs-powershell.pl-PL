---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223620"
---
# <span data-ttu-id="877d9-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="877d9-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="877d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="877d9-102">SYNOPSIS</span></span>
<span data-ttu-id="877d9-103">Pobiera miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="877d9-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="877d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="877d9-104">SYNTAX</span></span>

### <span data-ttu-id="877d9-105">S1</span><span class="sxs-lookup"><span data-stu-id="877d9-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="877d9-106">S2</span><span class="sxs-lookup"><span data-stu-id="877d9-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="877d9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="877d9-107">DESCRIPTION</span></span>
<span data-ttu-id="877d9-108">Polecenie cmdlet **Get-AzWebAppSlot** pobiera informacje o gnieździe aplikacji platformy Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="877d9-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="877d9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="877d9-109">EXAMPLES</span></span>

### <span data-ttu-id="877d9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="877d9-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="877d9-111">To polecenie umożliwia wyświetlenie gniazda o nazwie Slot001 z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="877d9-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="877d9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="877d9-112">PARAMETERS</span></span>

### <span data-ttu-id="877d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="877d9-113">-DefaultProfile</span></span>
<span data-ttu-id="877d9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="877d9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="877d9-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="877d9-115">-Name</span></span>
<span data-ttu-id="877d9-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="877d9-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="877d9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="877d9-117">-ResourceGroupName</span></span>
<span data-ttu-id="877d9-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="877d9-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877d9-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="877d9-119">-Slot</span></span>
<span data-ttu-id="877d9-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="877d9-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877d9-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="877d9-121">-WebApp</span></span>
<span data-ttu-id="877d9-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="877d9-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="877d9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="877d9-123">CommonParameters</span></span>
<span data-ttu-id="877d9-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="877d9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="877d9-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="877d9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="877d9-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="877d9-126">INPUTS</span></span>

### <span data-ttu-id="877d9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="877d9-127">System.String</span></span>

### <span data-ttu-id="877d9-128">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="877d9-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="877d9-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="877d9-129">OUTPUTS</span></span>

### <span data-ttu-id="877d9-130">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="877d9-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="877d9-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="877d9-131">NOTES</span></span>

## <span data-ttu-id="877d9-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="877d9-132">RELATED LINKS</span></span>

[<span data-ttu-id="877d9-133">Nowe — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="877d9-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="877d9-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="877d9-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="877d9-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="877d9-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="877d9-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="877d9-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="877d9-137">Start — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="877d9-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="877d9-138">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="877d9-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="877d9-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="877d9-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
