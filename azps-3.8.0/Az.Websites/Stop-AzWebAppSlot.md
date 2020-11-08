---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: eba40b4c372fd900ac42bead0e2c0b39305c91cc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051550"
---
# <span data-ttu-id="843c6-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="843c6-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="843c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="843c6-102">SYNOPSIS</span></span>
<span data-ttu-id="843c6-103">Zatrzymuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="843c6-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="843c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="843c6-104">SYNTAX</span></span>

### <span data-ttu-id="843c6-105">S1</span><span class="sxs-lookup"><span data-stu-id="843c6-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="843c6-106">S2</span><span class="sxs-lookup"><span data-stu-id="843c6-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="843c6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="843c6-107">DESCRIPTION</span></span>
<span data-ttu-id="843c6-108">Polecenie cmdlet **stop-AzWebAppSlot** zatrzymuje miejsce aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="843c6-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="843c6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="843c6-109">EXAMPLES</span></span>

### <span data-ttu-id="843c6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="843c6-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="843c6-111">To polecenie zatrzymuje Slot001 miejsca odnoszące się do aplikacji sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="843c6-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="843c6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="843c6-112">PARAMETERS</span></span>

### <span data-ttu-id="843c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="843c6-113">-DefaultProfile</span></span>
<span data-ttu-id="843c6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="843c6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="843c6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="843c6-115">-Name</span></span>
<span data-ttu-id="843c6-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="843c6-116">WebApp Name</span></span>

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

### <span data-ttu-id="843c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="843c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="843c6-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="843c6-118">Resource Group Name</span></span>

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

### <span data-ttu-id="843c6-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="843c6-119">-Slot</span></span>
<span data-ttu-id="843c6-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="843c6-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="843c6-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="843c6-121">-WebApp</span></span>
<span data-ttu-id="843c6-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="843c6-122">WebApp Object</span></span>

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

### <span data-ttu-id="843c6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="843c6-123">CommonParameters</span></span>
<span data-ttu-id="843c6-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="843c6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="843c6-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="843c6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="843c6-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="843c6-126">INPUTS</span></span>

### <span data-ttu-id="843c6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="843c6-127">System.String</span></span>

### <span data-ttu-id="843c6-128">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="843c6-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="843c6-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="843c6-129">OUTPUTS</span></span>

### <span data-ttu-id="843c6-130">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="843c6-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="843c6-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="843c6-131">NOTES</span></span>

## <span data-ttu-id="843c6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="843c6-132">RELATED LINKS</span></span>
