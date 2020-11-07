---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 9ac20046317fa7d070e69284696293e1f66ed486
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897757"
---
# <span data-ttu-id="0e090-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0e090-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="0e090-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e090-102">SYNOPSIS</span></span>
<span data-ttu-id="0e090-103">Pobiera miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0e090-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e090-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e090-104">SYNTAX</span></span>

### <span data-ttu-id="0e090-105">S1</span><span class="sxs-lookup"><span data-stu-id="0e090-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e090-106">S2</span><span class="sxs-lookup"><span data-stu-id="0e090-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e090-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0e090-107">DESCRIPTION</span></span>
<span data-ttu-id="0e090-108">Polecenie cmdlet **Get-AzureRmWebAppSlot** pobiera informacje o gnieździe aplikacji platformy Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0e090-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="0e090-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e090-109">EXAMPLES</span></span>

### <span data-ttu-id="0e090-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e090-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="0e090-111">To polecenie umożliwia wyświetlenie gniazda o nazwie Slot001 z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="0e090-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0e090-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e090-112">PARAMETERS</span></span>

### <span data-ttu-id="0e090-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e090-113">-DefaultProfile</span></span>
<span data-ttu-id="0e090-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e090-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e090-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e090-115">-Name</span></span>
<span data-ttu-id="0e090-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="0e090-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e090-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e090-117">-ResourceGroupName</span></span>
<span data-ttu-id="0e090-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0e090-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e090-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="0e090-119">-Slot</span></span>
<span data-ttu-id="0e090-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="0e090-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e090-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="0e090-121">-WebApp</span></span>
<span data-ttu-id="0e090-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="0e090-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e090-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e090-123">CommonParameters</span></span>
<span data-ttu-id="0e090-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e090-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e090-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e090-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e090-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e090-126">INPUTS</span></span>

### <span data-ttu-id="0e090-127">Klienta</span><span class="sxs-lookup"><span data-stu-id="0e090-127">Site</span></span>
<span data-ttu-id="0e090-128">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="0e090-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0e090-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e090-129">OUTPUTS</span></span>

## <span data-ttu-id="0e090-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e090-130">NOTES</span></span>

## <span data-ttu-id="0e090-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e090-131">RELATED LINKS</span></span>

[<span data-ttu-id="0e090-132">Nowe — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0e090-132">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="0e090-133">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0e090-133">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="0e090-134">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0e090-134">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="0e090-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0e090-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="0e090-136">Start — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0e090-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="0e090-137">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0e090-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="0e090-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0e090-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
