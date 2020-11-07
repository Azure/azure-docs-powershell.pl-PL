---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 033b0bd4458f20153ec1e9c876f12c7e7c368c0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891914"
---
# <span data-ttu-id="34611-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="34611-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="34611-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34611-102">SYNOPSIS</span></span>
<span data-ttu-id="34611-103">Pobiera miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="34611-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="34611-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34611-104">SYNTAX</span></span>

### <span data-ttu-id="34611-105">S1</span><span class="sxs-lookup"><span data-stu-id="34611-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34611-106">S2</span><span class="sxs-lookup"><span data-stu-id="34611-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34611-107">Opis</span><span class="sxs-lookup"><span data-stu-id="34611-107">DESCRIPTION</span></span>
<span data-ttu-id="34611-108">Polecenie cmdlet **Get-AzWebAppSlot** pobiera informacje o gnieździe aplikacji platformy Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="34611-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="34611-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34611-109">EXAMPLES</span></span>

### <span data-ttu-id="34611-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="34611-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="34611-111">To polecenie umożliwia wyświetlenie gniazda o nazwie Slot001 z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="34611-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="34611-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34611-112">PARAMETERS</span></span>

### <span data-ttu-id="34611-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34611-113">-DefaultProfile</span></span>
<span data-ttu-id="34611-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34611-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34611-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34611-115">-Name</span></span>
<span data-ttu-id="34611-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="34611-116">WebApp Name</span></span>

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

### <span data-ttu-id="34611-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34611-117">-ResourceGroupName</span></span>
<span data-ttu-id="34611-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="34611-118">Resource Group Name</span></span>

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

### <span data-ttu-id="34611-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="34611-119">-Slot</span></span>
<span data-ttu-id="34611-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="34611-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="34611-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="34611-121">-WebApp</span></span>
<span data-ttu-id="34611-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="34611-122">WebApp Object</span></span>

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

### <span data-ttu-id="34611-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34611-123">CommonParameters</span></span>
<span data-ttu-id="34611-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34611-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34611-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34611-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34611-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34611-126">INPUTS</span></span>

### <span data-ttu-id="34611-127">Klienta</span><span class="sxs-lookup"><span data-stu-id="34611-127">Site</span></span>
<span data-ttu-id="34611-128">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="34611-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="34611-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34611-129">OUTPUTS</span></span>

## <span data-ttu-id="34611-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34611-130">NOTES</span></span>

## <span data-ttu-id="34611-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34611-131">RELATED LINKS</span></span>

[<span data-ttu-id="34611-132">Nowe — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="34611-132">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="34611-133">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="34611-133">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="34611-134">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="34611-134">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="34611-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="34611-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="34611-136">Start — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="34611-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="34611-137">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="34611-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="34611-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="34611-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
