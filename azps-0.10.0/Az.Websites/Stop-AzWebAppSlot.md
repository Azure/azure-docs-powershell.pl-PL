---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 4ac4482cb5972553b1dad3972200d2f0eb032fe4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891801"
---
# <span data-ttu-id="31b04-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="31b04-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="31b04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31b04-102">SYNOPSIS</span></span>
<span data-ttu-id="31b04-103">Zatrzymuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="31b04-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="31b04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31b04-104">SYNTAX</span></span>

### <span data-ttu-id="31b04-105">S1</span><span class="sxs-lookup"><span data-stu-id="31b04-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31b04-106">S2</span><span class="sxs-lookup"><span data-stu-id="31b04-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31b04-107">Opis</span><span class="sxs-lookup"><span data-stu-id="31b04-107">DESCRIPTION</span></span>
<span data-ttu-id="31b04-108">Polecenie cmdlet **stop-AzWebAppSlot** zatrzymuje miejsce aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="31b04-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="31b04-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31b04-109">EXAMPLES</span></span>

### <span data-ttu-id="31b04-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="31b04-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="31b04-111">To polecenie zatrzymuje Slot001 miejsca odnoszące się do aplikacji sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="31b04-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="31b04-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31b04-112">PARAMETERS</span></span>

### <span data-ttu-id="31b04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b04-113">-DefaultProfile</span></span>
<span data-ttu-id="31b04-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31b04-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b04-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="31b04-115">-Name</span></span>
<span data-ttu-id="31b04-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="31b04-116">WebApp Name</span></span>

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

### <span data-ttu-id="31b04-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b04-117">-ResourceGroupName</span></span>
<span data-ttu-id="31b04-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="31b04-118">Resource Group Name</span></span>

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

### <span data-ttu-id="31b04-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="31b04-119">-Slot</span></span>
<span data-ttu-id="31b04-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="31b04-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="31b04-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="31b04-121">-WebApp</span></span>
<span data-ttu-id="31b04-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="31b04-122">WebApp Object</span></span>

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

### <span data-ttu-id="31b04-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b04-123">CommonParameters</span></span>
<span data-ttu-id="31b04-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b04-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b04-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b04-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b04-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31b04-126">INPUTS</span></span>

### <span data-ttu-id="31b04-127">Klienta</span><span class="sxs-lookup"><span data-stu-id="31b04-127">Site</span></span>
<span data-ttu-id="31b04-128">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="31b04-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="31b04-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31b04-129">OUTPUTS</span></span>

## <span data-ttu-id="31b04-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31b04-130">NOTES</span></span>

## <span data-ttu-id="31b04-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31b04-131">RELATED LINKS</span></span>

