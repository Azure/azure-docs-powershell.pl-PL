---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 615fcc228be9ef0e3e0d23c6463859c20ff7da11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707310"
---
# <span data-ttu-id="c9a20-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="c9a20-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="c9a20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9a20-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a20-103">Pobiera profil publikowania miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c9a20-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="c9a20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9a20-104">SYNTAX</span></span>

### <span data-ttu-id="c9a20-105">S1</span><span class="sxs-lookup"><span data-stu-id="c9a20-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9a20-106">S2</span><span class="sxs-lookup"><span data-stu-id="c9a20-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9a20-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c9a20-107">DESCRIPTION</span></span>
<span data-ttu-id="c9a20-108">Polecenie cmdlet **Get-AzWebAppSlotPublishingProfile** pobiera profil publikowania aplikacji sieci Web dla określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="c9a20-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="c9a20-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9a20-109">EXAMPLES</span></span>

### <span data-ttu-id="c9a20-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9a20-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="c9a20-111">To polecenie pobiera profil publikowania w formacie FTP dla gniazd Slot001 odnoszących się do aplikacji sieci Web ContosoWebApp skojarzonej z domyślnym grupą zasobów — sieć Web-zachód i zapisuje je w określonym pliku wyjściowym.</span><span class="sxs-lookup"><span data-stu-id="c9a20-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="c9a20-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9a20-112">PARAMETERS</span></span>

### <span data-ttu-id="c9a20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a20-113">-DefaultProfile</span></span>
<span data-ttu-id="c9a20-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9a20-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9a20-115">-Format</span><span class="sxs-lookup"><span data-stu-id="c9a20-115">-Format</span></span>
<span data-ttu-id="c9a20-116">Formaty</span><span class="sxs-lookup"><span data-stu-id="c9a20-116">Format</span></span>

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

### <span data-ttu-id="c9a20-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="c9a20-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="c9a20-118">Dołączanie punktów końcowych odzyskiwania po awarii w przypadku wartości prawda</span><span class="sxs-lookup"><span data-stu-id="c9a20-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9a20-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c9a20-119">-Name</span></span>
<span data-ttu-id="c9a20-120">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="c9a20-120">WebApp Name</span></span>

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

### <span data-ttu-id="c9a20-121">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="c9a20-121">-OutputFile</span></span>
<span data-ttu-id="c9a20-122">Plik wyjściowy</span><span class="sxs-lookup"><span data-stu-id="c9a20-122">Output File</span></span>

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

### <span data-ttu-id="c9a20-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9a20-123">-ResourceGroupName</span></span>
<span data-ttu-id="c9a20-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c9a20-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c9a20-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="c9a20-125">-Slot</span></span>
<span data-ttu-id="c9a20-126">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="c9a20-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c9a20-127">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="c9a20-127">-WebApp</span></span>
<span data-ttu-id="c9a20-128">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="c9a20-128">WebApp Object</span></span>

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

### <span data-ttu-id="c9a20-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a20-129">CommonParameters</span></span>
<span data-ttu-id="c9a20-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9a20-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a20-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9a20-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a20-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9a20-132">INPUTS</span></span>

### <span data-ttu-id="c9a20-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c9a20-133">System.String</span></span>

### <span data-ttu-id="c9a20-134">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="c9a20-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c9a20-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9a20-135">OUTPUTS</span></span>

### <span data-ttu-id="c9a20-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c9a20-136">System.String</span></span>

## <span data-ttu-id="c9a20-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9a20-137">NOTES</span></span>

## <span data-ttu-id="c9a20-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9a20-138">RELATED LINKS</span></span>

[<span data-ttu-id="c9a20-139">Resetowanie — AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="c9a20-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="c9a20-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c9a20-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="c9a20-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9a20-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)