---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 377e08f344256f6d744fec66f0b6b20f495d9309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051879"
---
# <span data-ttu-id="93246-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93246-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="93246-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93246-102">SYNOPSIS</span></span>

## <span data-ttu-id="93246-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93246-103">SYNTAX</span></span>

### <span data-ttu-id="93246-104">S1</span><span class="sxs-lookup"><span data-stu-id="93246-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93246-105">S2</span><span class="sxs-lookup"><span data-stu-id="93246-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93246-106">Opis</span><span class="sxs-lookup"><span data-stu-id="93246-106">DESCRIPTION</span></span>
<span data-ttu-id="93246-107">Polecenie cmdlet **restart-AzWebAppSlot** zostanie zatrzymane, a następnie rozpocznie się miejsce na platformie Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="93246-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="93246-108">Jeśli miejsce na aplikacja sieci Web jest zatrzymane, użyj polecenia cmdlet Start-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="93246-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="93246-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93246-109">EXAMPLES</span></span>

### <span data-ttu-id="93246-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="93246-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="93246-111">To polecenie uruchamia ponownie Slot001 gniazda dla aplikacji sieci Web ContosoWebApp skojarzonej z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="93246-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="93246-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93246-112">PARAMETERS</span></span>

### <span data-ttu-id="93246-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93246-113">-DefaultProfile</span></span>
<span data-ttu-id="93246-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="93246-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93246-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="93246-115">-Name</span></span>
<span data-ttu-id="93246-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="93246-116">WebApp Name</span></span>

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

### <span data-ttu-id="93246-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93246-117">-ResourceGroupName</span></span>
<span data-ttu-id="93246-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="93246-118">Resource Group Name</span></span>

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

### <span data-ttu-id="93246-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="93246-119">-Slot</span></span>
<span data-ttu-id="93246-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="93246-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="93246-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="93246-121">-WebApp</span></span>
<span data-ttu-id="93246-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="93246-122">WebApp Object</span></span>

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

### <span data-ttu-id="93246-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93246-123">CommonParameters</span></span>
<span data-ttu-id="93246-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93246-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93246-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93246-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93246-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93246-126">INPUTS</span></span>

### <span data-ttu-id="93246-127">System. String</span><span class="sxs-lookup"><span data-stu-id="93246-127">System.String</span></span>

### <span data-ttu-id="93246-128">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="93246-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="93246-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93246-129">OUTPUTS</span></span>

### <span data-ttu-id="93246-130">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="93246-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="93246-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93246-131">NOTES</span></span>

## <span data-ttu-id="93246-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93246-132">RELATED LINKS</span></span>

[<span data-ttu-id="93246-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93246-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="93246-134">Nowe — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93246-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="93246-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93246-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="93246-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93246-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="93246-137">Start — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93246-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="93246-138">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93246-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="93246-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="93246-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
