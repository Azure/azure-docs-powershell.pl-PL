---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: 08e5f0e1ba87f42f8a2893a63f8f853ece9870c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717995"
---
# <span data-ttu-id="7a276-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a276-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="7a276-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a276-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a276-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a276-103">SYNTAX</span></span>

### <span data-ttu-id="7a276-104">S1</span><span class="sxs-lookup"><span data-stu-id="7a276-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a276-105">S2</span><span class="sxs-lookup"><span data-stu-id="7a276-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a276-106">Opis</span><span class="sxs-lookup"><span data-stu-id="7a276-106">DESCRIPTION</span></span>
<span data-ttu-id="7a276-107">Polecenie cmdlet **restart-AzureRmWebAppSlot** zostanie zatrzymane, a następnie rozpocznie się miejsce na platformie Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7a276-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="7a276-108">Jeśli miejsce na aplikacja sieci Web jest zatrzymane, użyj polecenia cmdlet Start-AzureRmWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="7a276-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="7a276-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a276-109">EXAMPLES</span></span>

### <span data-ttu-id="7a276-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7a276-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="7a276-111">To polecenie uruchamia ponownie Slot001 gniazda dla aplikacji sieci Web ContosoWebApp skojarzonej z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="7a276-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="7a276-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a276-112">PARAMETERS</span></span>

### <span data-ttu-id="7a276-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a276-113">-DefaultProfile</span></span>
<span data-ttu-id="7a276-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a276-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a276-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a276-115">-Name</span></span>
<span data-ttu-id="7a276-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="7a276-116">WebApp Name</span></span>

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

### <span data-ttu-id="7a276-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a276-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a276-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7a276-118">Resource Group Name</span></span>

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

### <span data-ttu-id="7a276-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="7a276-119">-Slot</span></span>
<span data-ttu-id="7a276-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="7a276-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="7a276-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="7a276-121">-WebApp</span></span>
<span data-ttu-id="7a276-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="7a276-122">WebApp Object</span></span>

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

### <span data-ttu-id="7a276-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a276-123">CommonParameters</span></span>
<span data-ttu-id="7a276-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a276-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a276-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a276-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a276-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a276-126">INPUTS</span></span>

### <span data-ttu-id="7a276-127">Klienta</span><span class="sxs-lookup"><span data-stu-id="7a276-127">Site</span></span>
<span data-ttu-id="7a276-128">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="7a276-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7a276-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a276-129">OUTPUTS</span></span>

## <span data-ttu-id="7a276-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a276-130">NOTES</span></span>

## <span data-ttu-id="7a276-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a276-131">RELATED LINKS</span></span>

[<span data-ttu-id="7a276-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a276-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="7a276-133">Nowe — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a276-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="7a276-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a276-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="7a276-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a276-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="7a276-136">Start — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a276-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="7a276-137">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a276-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="7a276-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7a276-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
