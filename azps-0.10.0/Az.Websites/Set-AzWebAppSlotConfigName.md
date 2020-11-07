---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: ab00a1fbafc446affd30d7ae06dd0d48f0f0d04d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891829"
---
# <span data-ttu-id="c5297-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="c5297-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="c5297-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5297-102">SYNOPSIS</span></span>
<span data-ttu-id="c5297-103">Ustawianie nazw konfiguracji miejsca aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="c5297-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="c5297-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5297-104">SYNTAX</span></span>

### <span data-ttu-id="c5297-105">S1</span><span class="sxs-lookup"><span data-stu-id="c5297-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5297-106">S2</span><span class="sxs-lookup"><span data-stu-id="c5297-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5297-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c5297-107">DESCRIPTION</span></span>
<span data-ttu-id="c5297-108">Polecenie cmdlet **Set-AzWebAppSlotConfigName** oznacza ustawienia aplikacji i ciągi połączeń jako ustawienia gniazda</span><span class="sxs-lookup"><span data-stu-id="c5297-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="c5297-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5297-109">EXAMPLES</span></span>

### <span data-ttu-id="c5297-110">1:1</span><span class="sxs-lookup"><span data-stu-id="c5297-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="c5297-111">To polecenie usuwa wszystkie ustawienia aplikacji i parametry połączenia dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="c5297-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c5297-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5297-112">PARAMETERS</span></span>

### <span data-ttu-id="c5297-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="c5297-113">-AppSettingNames</span></span>
<span data-ttu-id="c5297-114">Tablica ciągów nazw ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5297-114">App Settings Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5297-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="c5297-115">-ConnectionStringNames</span></span>
<span data-ttu-id="c5297-116">Tablica ciągów nazw parametrów połączenia</span><span class="sxs-lookup"><span data-stu-id="c5297-116">Connection String Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5297-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5297-117">-DefaultProfile</span></span>
<span data-ttu-id="c5297-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5297-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5297-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c5297-119">-Name</span></span>
<span data-ttu-id="c5297-120">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5297-120">WebApp Name</span></span>

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

### <span data-ttu-id="c5297-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="c5297-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="c5297-122">Opcja Usuń wszystkie nazwy ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5297-122">Remove All App Setting Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5297-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="c5297-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="c5297-124">Opcja Usuń wszystkie nazwy parametrów połączenia</span><span class="sxs-lookup"><span data-stu-id="c5297-124">Remove All Connection String Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5297-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5297-125">-ResourceGroupName</span></span>
<span data-ttu-id="c5297-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c5297-126">Resource Group Name</span></span>

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

### <span data-ttu-id="c5297-127">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5297-127">-WebApp</span></span>
<span data-ttu-id="c5297-128">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5297-128">WebApp Object</span></span>

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

### <span data-ttu-id="c5297-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5297-129">CommonParameters</span></span>
<span data-ttu-id="c5297-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5297-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5297-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5297-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5297-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5297-132">INPUTS</span></span>

### <span data-ttu-id="c5297-133">Klienta</span><span class="sxs-lookup"><span data-stu-id="c5297-133">Site</span></span>
<span data-ttu-id="c5297-134">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="c5297-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c5297-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5297-135">OUTPUTS</span></span>

## <span data-ttu-id="c5297-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5297-136">NOTES</span></span>

## <span data-ttu-id="c5297-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5297-137">RELATED LINKS</span></span>

