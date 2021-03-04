---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: fed1be90af7aad2126b20dbe830f5069cc62e01f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994659"
---
# <span data-ttu-id="1d289-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1d289-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="1d289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d289-102">SYNOPSIS</span></span>
<span data-ttu-id="1d289-103">Pobiera profil publikowania miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1d289-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="1d289-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1d289-104">SYNTAX</span></span>

### <span data-ttu-id="1d289-105">S1</span><span class="sxs-lookup"><span data-stu-id="1d289-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d289-106">S2</span><span class="sxs-lookup"><span data-stu-id="1d289-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d289-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1d289-107">DESCRIPTION</span></span>
<span data-ttu-id="1d289-108">Polecenie **cmdlet Get-AzWebAppSlotPublishingProfile** pobiera profil publikowania aplikacji Sieci Web dla określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="1d289-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="1d289-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1d289-109">EXAMPLES</span></span>

### <span data-ttu-id="1d289-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1d289-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="1d289-111">To polecenie pobiera profil publikowania w formacie Ftp dla slotu Slot001 odnoszącego się do aplikacji Sieci Web ContosoWebApp skojarzonej z grupą zasobów Default-Web-WestUS i zapisuje go w określonym pliku wyjściowym.</span><span class="sxs-lookup"><span data-stu-id="1d289-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="1d289-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d289-112">PARAMETERS</span></span>

### <span data-ttu-id="1d289-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d289-113">-DefaultProfile</span></span>
<span data-ttu-id="1d289-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d289-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d289-115">— Format</span><span class="sxs-lookup"><span data-stu-id="1d289-115">-Format</span></span>
<span data-ttu-id="1d289-116">Format</span><span class="sxs-lookup"><span data-stu-id="1d289-116">Format</span></span>

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

### <span data-ttu-id="1d289-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="1d289-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="1d289-118">Uwzględnianie punktów końcowych odzyskiwania po awarii, jeśli ma wartość True (Prawda)</span><span class="sxs-lookup"><span data-stu-id="1d289-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="1d289-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1d289-119">-Name</span></span>
<span data-ttu-id="1d289-120">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="1d289-120">WebApp Name</span></span>

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

### <span data-ttu-id="1d289-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="1d289-121">-OutputFile</span></span>
<span data-ttu-id="1d289-122">Plik wyjściowy</span><span class="sxs-lookup"><span data-stu-id="1d289-122">Output File</span></span>

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

### <span data-ttu-id="1d289-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d289-123">-ResourceGroupName</span></span>
<span data-ttu-id="1d289-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1d289-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1d289-125">— Slot</span><span class="sxs-lookup"><span data-stu-id="1d289-125">-Slot</span></span>
<span data-ttu-id="1d289-126">Nazwa gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="1d289-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1d289-127">- WebApp</span><span class="sxs-lookup"><span data-stu-id="1d289-127">-WebApp</span></span>
<span data-ttu-id="1d289-128">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="1d289-128">WebApp Object</span></span>

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

### <span data-ttu-id="1d289-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d289-129">CommonParameters</span></span>
<span data-ttu-id="1d289-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d289-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d289-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d289-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d289-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d289-132">INPUTS</span></span>

### <span data-ttu-id="1d289-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1d289-133">System.String</span></span>

### <span data-ttu-id="1d289-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1d289-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1d289-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d289-135">OUTPUTS</span></span>

### <span data-ttu-id="1d289-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1d289-136">System.String</span></span>

## <span data-ttu-id="1d289-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1d289-137">NOTES</span></span>

## <span data-ttu-id="1d289-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d289-138">RELATED LINKS</span></span>

[<span data-ttu-id="1d289-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1d289-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="1d289-140">Get-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="1d289-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="1d289-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1d289-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
