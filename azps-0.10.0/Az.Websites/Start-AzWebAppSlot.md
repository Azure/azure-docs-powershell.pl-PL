---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: d843cf5eed70e230f81c704e9168fee917a77077
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891826"
---
# <span data-ttu-id="df6d1-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="df6d1-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="df6d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df6d1-102">SYNOPSIS</span></span>
<span data-ttu-id="df6d1-103">Uruchamia miejsce aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="df6d1-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="df6d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df6d1-104">SYNTAX</span></span>

### <span data-ttu-id="df6d1-105">S1</span><span class="sxs-lookup"><span data-stu-id="df6d1-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df6d1-106">S2</span><span class="sxs-lookup"><span data-stu-id="df6d1-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df6d1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="df6d1-107">DESCRIPTION</span></span>
<span data-ttu-id="df6d1-108">Polecenie cmdlet **Start-AzWebAppSlot** uruchamia miejsce aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="df6d1-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="df6d1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df6d1-109">EXAMPLES</span></span>

### <span data-ttu-id="df6d1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="df6d1-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="df6d1-111">To polecenie umożliwia uruchomienie gniazda o nazwie Slot001 należącego do aplikacji sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="df6d1-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="df6d1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df6d1-112">PARAMETERS</span></span>

### <span data-ttu-id="df6d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df6d1-113">-DefaultProfile</span></span>
<span data-ttu-id="df6d1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df6d1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df6d1-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df6d1-115">-Name</span></span>
<span data-ttu-id="df6d1-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="df6d1-116">WebApp Name</span></span>

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

### <span data-ttu-id="df6d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df6d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="df6d1-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="df6d1-118">Resource Group Name</span></span>

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

### <span data-ttu-id="df6d1-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="df6d1-119">-Slot</span></span>
<span data-ttu-id="df6d1-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="df6d1-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6d1-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="df6d1-121">-WebApp</span></span>
<span data-ttu-id="df6d1-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="df6d1-122">WebApp Object</span></span>

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

### <span data-ttu-id="df6d1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6d1-123">CommonParameters</span></span>
<span data-ttu-id="df6d1-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df6d1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df6d1-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df6d1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6d1-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df6d1-126">INPUTS</span></span>

### <span data-ttu-id="df6d1-127">Klienta</span><span class="sxs-lookup"><span data-stu-id="df6d1-127">Site</span></span>
<span data-ttu-id="df6d1-128">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="df6d1-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="df6d1-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df6d1-129">OUTPUTS</span></span>

## <span data-ttu-id="df6d1-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df6d1-130">NOTES</span></span>

## <span data-ttu-id="df6d1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df6d1-131">RELATED LINKS</span></span>

[<span data-ttu-id="df6d1-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="df6d1-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="df6d1-133">Nowe — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="df6d1-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="df6d1-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="df6d1-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="df6d1-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="df6d1-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="df6d1-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="df6d1-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="df6d1-137">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="df6d1-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="df6d1-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="df6d1-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
