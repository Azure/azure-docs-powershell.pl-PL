---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 9f0e48b20d19113290784d65b6bc78531dc7b2a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891838"
---
# <span data-ttu-id="2c1bc-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c1bc-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="2c1bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c1bc-102">SYNOPSIS</span></span>

## <span data-ttu-id="2c1bc-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c1bc-103">SYNTAX</span></span>

### <span data-ttu-id="2c1bc-104">S1</span><span class="sxs-lookup"><span data-stu-id="2c1bc-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c1bc-105">S2</span><span class="sxs-lookup"><span data-stu-id="2c1bc-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c1bc-106">Opis</span><span class="sxs-lookup"><span data-stu-id="2c1bc-106">DESCRIPTION</span></span>
<span data-ttu-id="2c1bc-107">Polecenie cmdlet **restart-AzWebAppSlot** zostanie zatrzymane, a następnie rozpocznie się miejsce na platformie Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="2c1bc-108">Jeśli miejsce na aplikacja sieci Web jest zatrzymane, użyj polecenia cmdlet Start-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="2c1bc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c1bc-109">EXAMPLES</span></span>

### <span data-ttu-id="2c1bc-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2c1bc-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="2c1bc-111">To polecenie uruchamia ponownie Slot001 gniazda dla aplikacji sieci Web ContosoWebApp skojarzonej z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="2c1bc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c1bc-112">PARAMETERS</span></span>

### <span data-ttu-id="2c1bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c1bc-113">-DefaultProfile</span></span>
<span data-ttu-id="2c1bc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c1bc-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c1bc-115">-Name</span></span>
<span data-ttu-id="2c1bc-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="2c1bc-116">WebApp Name</span></span>

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

### <span data-ttu-id="2c1bc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c1bc-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c1bc-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2c1bc-118">Resource Group Name</span></span>

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

### <span data-ttu-id="2c1bc-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="2c1bc-119">-Slot</span></span>
<span data-ttu-id="2c1bc-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="2c1bc-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2c1bc-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="2c1bc-121">-WebApp</span></span>
<span data-ttu-id="2c1bc-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="2c1bc-122">WebApp Object</span></span>

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

### <span data-ttu-id="2c1bc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c1bc-123">CommonParameters</span></span>
<span data-ttu-id="2c1bc-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c1bc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c1bc-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c1bc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c1bc-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c1bc-126">INPUTS</span></span>

### <span data-ttu-id="2c1bc-127">Klienta</span><span class="sxs-lookup"><span data-stu-id="2c1bc-127">Site</span></span>
<span data-ttu-id="2c1bc-128">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="2c1bc-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2c1bc-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c1bc-129">OUTPUTS</span></span>

## <span data-ttu-id="2c1bc-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c1bc-130">NOTES</span></span>

## <span data-ttu-id="2c1bc-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c1bc-131">RELATED LINKS</span></span>

[<span data-ttu-id="2c1bc-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c1bc-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="2c1bc-133">Nowe — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c1bc-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="2c1bc-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c1bc-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="2c1bc-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c1bc-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="2c1bc-136">Start — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c1bc-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="2c1bc-137">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c1bc-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="2c1bc-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2c1bc-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
