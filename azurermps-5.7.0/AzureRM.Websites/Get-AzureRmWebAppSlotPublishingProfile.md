---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: dbbab46f0363273e53af93db94cb283866af70b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542111"
---
# <span data-ttu-id="71512-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="71512-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="71512-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71512-102">SYNOPSIS</span></span>
<span data-ttu-id="71512-103">Pobiera profil publikowania miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="71512-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71512-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71512-104">SYNTAX</span></span>

### <span data-ttu-id="71512-105">S1</span><span class="sxs-lookup"><span data-stu-id="71512-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71512-106">S2</span><span class="sxs-lookup"><span data-stu-id="71512-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71512-107">Opis</span><span class="sxs-lookup"><span data-stu-id="71512-107">DESCRIPTION</span></span>
<span data-ttu-id="71512-108">Polecenie cmdlet **Get-AzureRmWebAppSlotPublishingProfile** pobiera profil publikowania aplikacji sieci Web dla określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="71512-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="71512-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71512-109">EXAMPLES</span></span>

### <span data-ttu-id="71512-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71512-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="71512-111">To polecenie pobiera profil publikowania w formacie FTP dla gniazd Slot001 odnoszących się do aplikacji sieci Web ContosoWebApp skojarzonej z domyślnym grupą zasobów — sieć Web-zachód i zapisuje je w określonym pliku wyjściowym.</span><span class="sxs-lookup"><span data-stu-id="71512-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="71512-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71512-112">PARAMETERS</span></span>

### <span data-ttu-id="71512-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71512-113">-DefaultProfile</span></span>
<span data-ttu-id="71512-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71512-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71512-115">-Format</span><span class="sxs-lookup"><span data-stu-id="71512-115">-Format</span></span>
<span data-ttu-id="71512-116">Formaty</span><span class="sxs-lookup"><span data-stu-id="71512-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71512-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71512-117">-Name</span></span>
<span data-ttu-id="71512-118">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="71512-118">WebApp Name</span></span>

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

### <span data-ttu-id="71512-119">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="71512-119">-OutputFile</span></span>
<span data-ttu-id="71512-120">Plik wyjściowy</span><span class="sxs-lookup"><span data-stu-id="71512-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71512-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71512-121">-ResourceGroupName</span></span>
<span data-ttu-id="71512-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="71512-122">Resource Group Name</span></span>

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

### <span data-ttu-id="71512-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="71512-123">-Slot</span></span>
<span data-ttu-id="71512-124">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="71512-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="71512-125">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="71512-125">-WebApp</span></span>
<span data-ttu-id="71512-126">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="71512-126">WebApp Object</span></span>

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

### <span data-ttu-id="71512-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71512-127">CommonParameters</span></span>
<span data-ttu-id="71512-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71512-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71512-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71512-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71512-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71512-130">INPUTS</span></span>

### <span data-ttu-id="71512-131">Klienta</span><span class="sxs-lookup"><span data-stu-id="71512-131">Site</span></span>
<span data-ttu-id="71512-132">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="71512-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="71512-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71512-133">OUTPUTS</span></span>

## <span data-ttu-id="71512-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71512-134">NOTES</span></span>

## <span data-ttu-id="71512-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71512-135">RELATED LINKS</span></span>

[<span data-ttu-id="71512-136">Resetowanie — AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="71512-136">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="71512-137">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71512-137">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="71512-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="71512-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)