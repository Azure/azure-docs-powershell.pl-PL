---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 9c23484fa5f8b45548985645db45872fcc63f66b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550459"
---
# <span data-ttu-id="f69db-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f69db-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f69db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f69db-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f69db-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f69db-103">SYNTAX</span></span>

### <span data-ttu-id="f69db-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f69db-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="f69db-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f69db-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="f69db-106">Opis</span><span class="sxs-lookup"><span data-stu-id="f69db-106">DESCRIPTION</span></span>
<span data-ttu-id="f69db-107">Polecenie cmdlet **Edit-AzureRmWebAppBackupConfiguration** umożliwia edytowanie bieżącej kopii zapasowej konfiguracji dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f69db-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="f69db-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f69db-108">EXAMPLES</span></span>

## <span data-ttu-id="f69db-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f69db-109">PARAMETERS</span></span>

### <span data-ttu-id="f69db-110">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="f69db-110">-Databases</span></span>
<span data-ttu-id="f69db-111">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="f69db-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f69db-112">-DefaultProfile</span></span>
<span data-ttu-id="f69db-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f69db-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f69db-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="f69db-114">-FrequencyInterval</span></span>
<span data-ttu-id="f69db-115">Interwał częstotliwości</span><span class="sxs-lookup"><span data-stu-id="f69db-115">Frequency Interval</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="f69db-116">-FrequencyUnit</span></span>
<span data-ttu-id="f69db-117">Jednostka częstotliwości</span><span class="sxs-lookup"><span data-stu-id="f69db-117">Frequency Unit</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="f69db-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="f69db-119">Zachowywanie co najmniej jednej opcji kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="f69db-119">Keep At Least One Backup Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f69db-120">-Name</span></span>
<span data-ttu-id="f69db-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="f69db-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f69db-122">-ResourceGroupName</span></span>
<span data-ttu-id="f69db-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f69db-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="f69db-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="f69db-125">Okres przechowywania w dniach</span><span class="sxs-lookup"><span data-stu-id="f69db-125">Retention Period In Days</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="f69db-126">-Slot</span></span>
<span data-ttu-id="f69db-127">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="f69db-127">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f69db-128">-StartTime</span></span>
<span data-ttu-id="f69db-129">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="f69db-129">StartTime in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="f69db-130">-StorageAccountUrl</span></span>
<span data-ttu-id="f69db-131">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="f69db-131">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-132">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="f69db-132">-WebApp</span></span>
<span data-ttu-id="f69db-133">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="f69db-133">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69db-134">CommonParameters</span></span>
<span data-ttu-id="f69db-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f69db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69db-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f69db-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69db-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f69db-137">INPUTS</span></span>

### <span data-ttu-id="f69db-138">Klienta</span><span class="sxs-lookup"><span data-stu-id="f69db-138">Site</span></span>
<span data-ttu-id="f69db-139">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="f69db-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f69db-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f69db-140">OUTPUTS</span></span>

### <span data-ttu-id="f69db-141">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f69db-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f69db-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f69db-142">NOTES</span></span>

## <span data-ttu-id="f69db-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f69db-143">RELATED LINKS</span></span>

[<span data-ttu-id="f69db-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f69db-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


