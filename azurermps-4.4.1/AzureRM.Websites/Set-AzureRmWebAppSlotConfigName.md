---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 3ed7bd25c394c2bef5cb3636a4f8c238f45a3558
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525445"
---
# <span data-ttu-id="763ae-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="763ae-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="763ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="763ae-102">SYNOPSIS</span></span>
<span data-ttu-id="763ae-103">Ustawianie nazw konfiguracji miejsca aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="763ae-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="763ae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="763ae-104">SYNTAX</span></span>

### <span data-ttu-id="763ae-105">S1</span><span class="sxs-lookup"><span data-stu-id="763ae-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="763ae-106">S2</span><span class="sxs-lookup"><span data-stu-id="763ae-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="763ae-107">Opis</span><span class="sxs-lookup"><span data-stu-id="763ae-107">DESCRIPTION</span></span>
<span data-ttu-id="763ae-108">Polecenie cmdlet **Set-AzureRmWebAppSlotConfigName** oznacza ustawienia aplikacji i ciągi połączeń jako ustawienia gniazda</span><span class="sxs-lookup"><span data-stu-id="763ae-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="763ae-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="763ae-109">EXAMPLES</span></span>

### <span data-ttu-id="763ae-110">1:1</span><span class="sxs-lookup"><span data-stu-id="763ae-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="763ae-111">To polecenie usuwa wszystkie ustawienia aplikacji i parametry połączenia dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="763ae-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="763ae-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="763ae-112">PARAMETERS</span></span>

### <span data-ttu-id="763ae-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="763ae-113">-AppSettingNames</span></span>
<span data-ttu-id="763ae-114">Tablica ciągów nazw ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="763ae-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="763ae-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="763ae-115">-ConnectionStringNames</span></span>
<span data-ttu-id="763ae-116">Tablica ciągów nazw parametrów połączenia</span><span class="sxs-lookup"><span data-stu-id="763ae-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="763ae-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="763ae-117">-Name</span></span>
<span data-ttu-id="763ae-118">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="763ae-118">WebApp Name</span></span>

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

### <span data-ttu-id="763ae-119">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="763ae-119">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="763ae-120">Opcja Usuń wszystkie nazwy ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="763ae-120">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="763ae-121">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="763ae-121">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="763ae-122">Opcja Usuń wszystkie nazwy parametrów połączenia</span><span class="sxs-lookup"><span data-stu-id="763ae-122">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="763ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="763ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="763ae-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="763ae-124">Resource Group Name</span></span>

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

### <span data-ttu-id="763ae-125">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="763ae-125">-WebApp</span></span>
<span data-ttu-id="763ae-126">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="763ae-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="763ae-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="763ae-127">-DefaultProfile</span></span>
<span data-ttu-id="763ae-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="763ae-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="763ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="763ae-129">CommonParameters</span></span>
<span data-ttu-id="763ae-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="763ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="763ae-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="763ae-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="763ae-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="763ae-132">INPUTS</span></span>

### <span data-ttu-id="763ae-133">Klienta</span><span class="sxs-lookup"><span data-stu-id="763ae-133">Site</span></span>
<span data-ttu-id="763ae-134">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="763ae-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="763ae-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="763ae-135">OUTPUTS</span></span>

## <span data-ttu-id="763ae-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="763ae-136">NOTES</span></span>

## <span data-ttu-id="763ae-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="763ae-137">RELATED LINKS</span></span>

