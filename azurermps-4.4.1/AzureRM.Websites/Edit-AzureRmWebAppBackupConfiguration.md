---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: d7fd26d81b683095fb08c1dbca3226761f047d4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542788"
---
# <span data-ttu-id="74b63-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="74b63-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="74b63-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74b63-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74b63-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74b63-103">SYNTAX</span></span>

### <span data-ttu-id="74b63-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="74b63-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="74b63-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="74b63-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="74b63-106">Opis</span><span class="sxs-lookup"><span data-stu-id="74b63-106">DESCRIPTION</span></span>
<span data-ttu-id="74b63-107">Polecenie cmdlet **Edit-AzureRmWebAppBackupConfiguration** umożliwia edytowanie bieżącej kopii zapasowej konfiguracji dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="74b63-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="74b63-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74b63-108">EXAMPLES</span></span>

## <span data-ttu-id="74b63-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74b63-109">PARAMETERS</span></span>

### <span data-ttu-id="74b63-110">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="74b63-110">-Databases</span></span>
<span data-ttu-id="74b63-111">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="74b63-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b63-112">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="74b63-112">-FrequencyInterval</span></span>
<span data-ttu-id="74b63-113">Interwał częstotliwości</span><span class="sxs-lookup"><span data-stu-id="74b63-113">Frequency Interval</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b63-114">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="74b63-114">-FrequencyUnit</span></span>
<span data-ttu-id="74b63-115">Jednostka częstotliwości</span><span class="sxs-lookup"><span data-stu-id="74b63-115">Frequency Unit</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b63-116">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="74b63-116">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="74b63-117">Zachowywanie co najmniej jednej opcji kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="74b63-117">Keep At Least One Backup Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b63-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74b63-118">-Name</span></span>
<span data-ttu-id="74b63-119">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="74b63-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b63-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b63-120">-ResourceGroupName</span></span>
<span data-ttu-id="74b63-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="74b63-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b63-122">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="74b63-122">-RetentionPeriodInDays</span></span>
<span data-ttu-id="74b63-123">Okres przechowywania w dniach</span><span class="sxs-lookup"><span data-stu-id="74b63-123">Retention Period In Days</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b63-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="74b63-124">-Slot</span></span>
<span data-ttu-id="74b63-125">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="74b63-125">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b63-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="74b63-126">-StartTime</span></span>
<span data-ttu-id="74b63-127">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="74b63-127">StartTime in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b63-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="74b63-128">-StorageAccountUrl</span></span>
<span data-ttu-id="74b63-129">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="74b63-129">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b63-130">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="74b63-130">-WebApp</span></span>
<span data-ttu-id="74b63-131">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="74b63-131">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74b63-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b63-132">-DefaultProfile</span></span>
<span data-ttu-id="74b63-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74b63-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74b63-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b63-134">CommonParameters</span></span>
<span data-ttu-id="74b63-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74b63-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b63-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74b63-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b63-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74b63-137">INPUTS</span></span>

### <span data-ttu-id="74b63-138">Klienta</span><span class="sxs-lookup"><span data-stu-id="74b63-138">Site</span></span>
<span data-ttu-id="74b63-139">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="74b63-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="74b63-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74b63-140">OUTPUTS</span></span>

### <span data-ttu-id="74b63-141">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="74b63-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="74b63-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74b63-142">NOTES</span></span>

## <span data-ttu-id="74b63-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74b63-143">RELATED LINKS</span></span>

[<span data-ttu-id="74b63-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="74b63-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


