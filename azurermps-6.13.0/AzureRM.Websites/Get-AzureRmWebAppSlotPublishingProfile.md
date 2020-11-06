---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 29ef83bf3ed0f423686e7ddf84bc82555bd09572
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524210"
---
# <span data-ttu-id="76dff-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="76dff-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="76dff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76dff-102">SYNOPSIS</span></span>
<span data-ttu-id="76dff-103">Pobiera profil publikowania miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="76dff-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76dff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76dff-104">SYNTAX</span></span>

### <span data-ttu-id="76dff-105">S1</span><span class="sxs-lookup"><span data-stu-id="76dff-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76dff-106">S2</span><span class="sxs-lookup"><span data-stu-id="76dff-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76dff-107">Opis</span><span class="sxs-lookup"><span data-stu-id="76dff-107">DESCRIPTION</span></span>
<span data-ttu-id="76dff-108">Polecenie cmdlet **Get-AzureRmWebAppSlotPublishingProfile** pobiera profil publikowania aplikacji sieci Web dla określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="76dff-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="76dff-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76dff-109">EXAMPLES</span></span>

### <span data-ttu-id="76dff-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76dff-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="76dff-111">To polecenie pobiera profil publikowania w formacie FTP dla gniazd Slot001 odnoszących się do aplikacji sieci Web ContosoWebApp skojarzonej z domyślnym grupą zasobów — sieć Web-zachód i zapisuje je w określonym pliku wyjściowym.</span><span class="sxs-lookup"><span data-stu-id="76dff-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="76dff-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76dff-112">PARAMETERS</span></span>

### <span data-ttu-id="76dff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76dff-113">-DefaultProfile</span></span>
<span data-ttu-id="76dff-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76dff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76dff-115">-Format</span><span class="sxs-lookup"><span data-stu-id="76dff-115">-Format</span></span>
<span data-ttu-id="76dff-116">Formaty</span><span class="sxs-lookup"><span data-stu-id="76dff-116">Format</span></span>

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

### <span data-ttu-id="76dff-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="76dff-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="76dff-118">Dołączanie punktów końcowych odzyskiwania po awarii w przypadku wartości prawda</span><span class="sxs-lookup"><span data-stu-id="76dff-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dff-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76dff-119">-Name</span></span>
<span data-ttu-id="76dff-120">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="76dff-120">WebApp Name</span></span>

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

### <span data-ttu-id="76dff-121">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="76dff-121">-OutputFile</span></span>
<span data-ttu-id="76dff-122">Plik wyjściowy</span><span class="sxs-lookup"><span data-stu-id="76dff-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76dff-123">-ResourceGroupName</span></span>
<span data-ttu-id="76dff-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="76dff-124">Resource Group Name</span></span>

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

### <span data-ttu-id="76dff-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="76dff-125">-Slot</span></span>
<span data-ttu-id="76dff-126">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="76dff-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="76dff-127">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="76dff-127">-WebApp</span></span>
<span data-ttu-id="76dff-128">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="76dff-128">WebApp Object</span></span>

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

### <span data-ttu-id="76dff-129">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="76dff-129">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="76dff-130">Dołączanie punktów końcowych odzyskiwania po awarii w przypadku wartości prawda</span><span class="sxs-lookup"><span data-stu-id="76dff-130">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76dff-131">CommonParameters</span></span>
<span data-ttu-id="76dff-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76dff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76dff-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76dff-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76dff-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76dff-134">INPUTS</span></span>

### <span data-ttu-id="76dff-135">System. String</span><span class="sxs-lookup"><span data-stu-id="76dff-135">System.String</span></span>

### <span data-ttu-id="76dff-136">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="76dff-136">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="76dff-137">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="76dff-137">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="76dff-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76dff-138">OUTPUTS</span></span>

### <span data-ttu-id="76dff-139">System. String</span><span class="sxs-lookup"><span data-stu-id="76dff-139">System.String</span></span>

## <span data-ttu-id="76dff-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76dff-140">NOTES</span></span>

## <span data-ttu-id="76dff-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76dff-141">RELATED LINKS</span></span>

[<span data-ttu-id="76dff-142">Resetowanie — AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="76dff-142">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="76dff-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="76dff-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="76dff-144">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="76dff-144">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
