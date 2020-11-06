---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: d8ccd8f1011a73068c24323bb86e39340dfc9573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544615"
---
# <span data-ttu-id="7a709-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="7a709-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="7a709-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a709-102">SYNOPSIS</span></span>
<span data-ttu-id="7a709-103">Pobiera profil publikowania miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7a709-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a709-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a709-104">SYNTAX</span></span>

### <span data-ttu-id="7a709-105">S1</span><span class="sxs-lookup"><span data-stu-id="7a709-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a709-106">S2</span><span class="sxs-lookup"><span data-stu-id="7a709-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a709-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7a709-107">DESCRIPTION</span></span>
<span data-ttu-id="7a709-108">Polecenie cmdlet **Get-AzureRmWebAppSlotPublishingProfile** pobiera profil publikowania aplikacji sieci Web dla określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="7a709-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="7a709-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a709-109">EXAMPLES</span></span>

### <span data-ttu-id="7a709-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7a709-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="7a709-111">To polecenie pobiera profil publikowania w formacie FTP dla gniazd Slot001 odnoszących się do aplikacji sieci Web ContosoWebApp skojarzonej z domyślnym grupą zasobów — sieć Web-zachód i zapisuje je w określonym pliku wyjściowym.</span><span class="sxs-lookup"><span data-stu-id="7a709-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="7a709-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a709-112">PARAMETERS</span></span>

### <span data-ttu-id="7a709-113">-Format</span><span class="sxs-lookup"><span data-stu-id="7a709-113">-Format</span></span>
<span data-ttu-id="7a709-114">Formaty</span><span class="sxs-lookup"><span data-stu-id="7a709-114">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a709-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a709-115">-Name</span></span>
<span data-ttu-id="7a709-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="7a709-116">WebApp Name</span></span>

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

### <span data-ttu-id="7a709-117">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="7a709-117">-OutputFile</span></span>
<span data-ttu-id="7a709-118">Plik wyjściowy</span><span class="sxs-lookup"><span data-stu-id="7a709-118">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a709-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a709-119">-ResourceGroupName</span></span>
<span data-ttu-id="7a709-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7a709-120">Resource Group Name</span></span>

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

### <span data-ttu-id="7a709-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="7a709-121">-Slot</span></span>
<span data-ttu-id="7a709-122">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="7a709-122">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a709-123">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="7a709-123">-WebApp</span></span>
<span data-ttu-id="7a709-124">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="7a709-124">WebApp Object</span></span>

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

### <span data-ttu-id="7a709-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a709-125">-DefaultProfile</span></span>
<span data-ttu-id="7a709-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a709-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a709-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a709-127">CommonParameters</span></span>
<span data-ttu-id="7a709-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a709-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a709-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a709-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a709-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a709-130">INPUTS</span></span>

### <span data-ttu-id="7a709-131">Klienta</span><span class="sxs-lookup"><span data-stu-id="7a709-131">Site</span></span>
<span data-ttu-id="7a709-132">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="7a709-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7a709-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a709-133">OUTPUTS</span></span>

## <span data-ttu-id="7a709-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a709-134">NOTES</span></span>

## <span data-ttu-id="7a709-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a709-135">RELATED LINKS</span></span>

[<span data-ttu-id="7a709-136">Resetowanie — AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="7a709-136">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="7a709-137">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a709-137">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="7a709-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7a709-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
