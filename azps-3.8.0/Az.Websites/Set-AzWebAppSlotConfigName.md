---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: a2c57ebe6f85209596628dffe9de88ca260bbafa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051565"
---
# <span data-ttu-id="40249-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="40249-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="40249-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40249-102">SYNOPSIS</span></span>
<span data-ttu-id="40249-103">Ustawianie nazw konfiguracji miejsca aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="40249-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="40249-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40249-104">SYNTAX</span></span>

### <span data-ttu-id="40249-105">S1</span><span class="sxs-lookup"><span data-stu-id="40249-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40249-106">S2</span><span class="sxs-lookup"><span data-stu-id="40249-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40249-107">Opis</span><span class="sxs-lookup"><span data-stu-id="40249-107">DESCRIPTION</span></span>
<span data-ttu-id="40249-108">Polecenie cmdlet **Set-AzWebAppSlotConfigName** oznacza ustawienia aplikacji i ciągi połączeń jako ustawienia gniazda</span><span class="sxs-lookup"><span data-stu-id="40249-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="40249-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40249-109">EXAMPLES</span></span>

### <span data-ttu-id="40249-110">1:1</span><span class="sxs-lookup"><span data-stu-id="40249-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="40249-111">To polecenie usuwa wszystkie ustawienia aplikacji i parametry połączenia dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="40249-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="40249-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40249-112">PARAMETERS</span></span>

### <span data-ttu-id="40249-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="40249-113">-AppSettingNames</span></span>
<span data-ttu-id="40249-114">Tablica ciągów nazw ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="40249-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="40249-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="40249-115">-ConnectionStringNames</span></span>
<span data-ttu-id="40249-116">Tablica ciągów nazw parametrów połączenia</span><span class="sxs-lookup"><span data-stu-id="40249-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="40249-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40249-117">-DefaultProfile</span></span>
<span data-ttu-id="40249-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40249-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40249-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40249-119">-Name</span></span>
<span data-ttu-id="40249-120">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="40249-120">WebApp Name</span></span>

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

### <span data-ttu-id="40249-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="40249-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="40249-122">Opcja Usuń wszystkie nazwy ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="40249-122">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="40249-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="40249-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="40249-124">Opcja Usuń wszystkie nazwy parametrów połączenia</span><span class="sxs-lookup"><span data-stu-id="40249-124">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="40249-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40249-125">-ResourceGroupName</span></span>
<span data-ttu-id="40249-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="40249-126">Resource Group Name</span></span>

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

### <span data-ttu-id="40249-127">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="40249-127">-WebApp</span></span>
<span data-ttu-id="40249-128">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="40249-128">WebApp Object</span></span>

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

### <span data-ttu-id="40249-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40249-129">CommonParameters</span></span>
<span data-ttu-id="40249-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40249-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40249-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40249-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40249-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40249-132">INPUTS</span></span>

### <span data-ttu-id="40249-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="40249-133">System.String[]</span></span>

### <span data-ttu-id="40249-134">System. String</span><span class="sxs-lookup"><span data-stu-id="40249-134">System.String</span></span>

### <span data-ttu-id="40249-135">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="40249-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="40249-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40249-136">OUTPUTS</span></span>

### <span data-ttu-id="40249-137">Microsoft. Azure. Management. Web. MODELES. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="40249-137">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="40249-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40249-138">NOTES</span></span>

## <span data-ttu-id="40249-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40249-139">RELATED LINKS</span></span>
