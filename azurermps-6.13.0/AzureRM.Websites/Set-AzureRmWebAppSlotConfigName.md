---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 75c134b162636f94b00cf6692f4e9df120930dcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546291"
---
# <span data-ttu-id="e8960-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="e8960-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="e8960-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8960-102">SYNOPSIS</span></span>
<span data-ttu-id="e8960-103">Ustawianie nazw konfiguracji miejsca aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="e8960-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8960-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8960-104">SYNTAX</span></span>

### <span data-ttu-id="e8960-105">S1</span><span class="sxs-lookup"><span data-stu-id="e8960-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8960-106">S2</span><span class="sxs-lookup"><span data-stu-id="e8960-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8960-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e8960-107">DESCRIPTION</span></span>
<span data-ttu-id="e8960-108">Polecenie cmdlet **Set-AzureRmWebAppSlotConfigName** oznacza ustawienia aplikacji i ciągi połączeń jako ustawienia gniazda</span><span class="sxs-lookup"><span data-stu-id="e8960-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="e8960-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8960-109">EXAMPLES</span></span>

### <span data-ttu-id="e8960-110">1:1</span><span class="sxs-lookup"><span data-stu-id="e8960-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="e8960-111">To polecenie usuwa wszystkie ustawienia aplikacji i parametry połączenia dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="e8960-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="e8960-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8960-112">PARAMETERS</span></span>

### <span data-ttu-id="e8960-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="e8960-113">-AppSettingNames</span></span>
<span data-ttu-id="e8960-114">Tablica ciągów nazw ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="e8960-114">App Settings Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8960-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="e8960-115">-ConnectionStringNames</span></span>
<span data-ttu-id="e8960-116">Tablica ciągów nazw parametrów połączenia</span><span class="sxs-lookup"><span data-stu-id="e8960-116">Connection String Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8960-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8960-117">-DefaultProfile</span></span>
<span data-ttu-id="e8960-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8960-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8960-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8960-119">-Name</span></span>
<span data-ttu-id="e8960-120">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="e8960-120">WebApp Name</span></span>

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

### <span data-ttu-id="e8960-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="e8960-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="e8960-122">Opcja Usuń wszystkie nazwy ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="e8960-122">Remove All App Setting Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8960-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="e8960-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="e8960-124">Opcja Usuń wszystkie nazwy parametrów połączenia</span><span class="sxs-lookup"><span data-stu-id="e8960-124">Remove All Connection String Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8960-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8960-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8960-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e8960-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e8960-127">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="e8960-127">-WebApp</span></span>
<span data-ttu-id="e8960-128">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="e8960-128">WebApp Object</span></span>

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

### <span data-ttu-id="e8960-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8960-129">CommonParameters</span></span>
<span data-ttu-id="e8960-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8960-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8960-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8960-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8960-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8960-132">INPUTS</span></span>

### <span data-ttu-id="e8960-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="e8960-133">System.String[]</span></span>

### <span data-ttu-id="e8960-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e8960-134">System.String</span></span>

### <span data-ttu-id="e8960-135">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="e8960-135">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="e8960-136">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e8960-136">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="e8960-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8960-137">OUTPUTS</span></span>

### <span data-ttu-id="e8960-138">Microsoft. Azure. Management. Web. MODELES. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="e8960-138">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="e8960-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8960-139">NOTES</span></span>

## <span data-ttu-id="e8960-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8960-140">RELATED LINKS</span></span>
