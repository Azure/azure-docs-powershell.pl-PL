---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: 2d1c4fe635e6d4bc509f82f1af376ee0f662217a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546324"
---
# <span data-ttu-id="6aca2-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6aca2-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="6aca2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6aca2-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6aca2-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6aca2-103">SYNTAX</span></span>

### <span data-ttu-id="6aca2-104">S1</span><span class="sxs-lookup"><span data-stu-id="6aca2-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6aca2-105">S2</span><span class="sxs-lookup"><span data-stu-id="6aca2-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aca2-106">Opis</span><span class="sxs-lookup"><span data-stu-id="6aca2-106">DESCRIPTION</span></span>
<span data-ttu-id="6aca2-107">Polecenie cmdlet **restart-AzureRmWebAppSlot** zostanie zatrzymane, a następnie rozpocznie się miejsce na platformie Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6aca2-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="6aca2-108">Jeśli miejsce na aplikacja sieci Web jest zatrzymane, użyj polecenia cmdlet Start-AzureRmWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="6aca2-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="6aca2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6aca2-109">EXAMPLES</span></span>

### <span data-ttu-id="6aca2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6aca2-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="6aca2-111">To polecenie uruchamia ponownie Slot001 gniazda dla aplikacji sieci Web ContosoWebApp skojarzonej z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="6aca2-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="6aca2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6aca2-112">PARAMETERS</span></span>

### <span data-ttu-id="6aca2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aca2-113">-DefaultProfile</span></span>
<span data-ttu-id="6aca2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6aca2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aca2-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6aca2-115">-Name</span></span>
<span data-ttu-id="6aca2-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="6aca2-116">WebApp Name</span></span>

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

### <span data-ttu-id="6aca2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aca2-117">-ResourceGroupName</span></span>
<span data-ttu-id="6aca2-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6aca2-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6aca2-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="6aca2-119">-Slot</span></span>
<span data-ttu-id="6aca2-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="6aca2-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="6aca2-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="6aca2-121">-WebApp</span></span>
<span data-ttu-id="6aca2-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="6aca2-122">WebApp Object</span></span>

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

### <span data-ttu-id="6aca2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aca2-123">CommonParameters</span></span>
<span data-ttu-id="6aca2-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aca2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aca2-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aca2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aca2-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6aca2-126">INPUTS</span></span>

### <span data-ttu-id="6aca2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6aca2-127">System.String</span></span>

### <span data-ttu-id="6aca2-128">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="6aca2-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="6aca2-129">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6aca2-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="6aca2-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6aca2-130">OUTPUTS</span></span>

### <span data-ttu-id="6aca2-131">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="6aca2-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="6aca2-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6aca2-132">NOTES</span></span>

## <span data-ttu-id="6aca2-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6aca2-133">RELATED LINKS</span></span>

[<span data-ttu-id="6aca2-134">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6aca2-134">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="6aca2-135">Nowe — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6aca2-135">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="6aca2-136">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6aca2-136">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="6aca2-137">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6aca2-137">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="6aca2-138">Start — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6aca2-138">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="6aca2-139">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6aca2-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="6aca2-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6aca2-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
