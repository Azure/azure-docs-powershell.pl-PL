---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
ms.openlocfilehash: 6396da138a0bafd54241f859c107601a1ce14b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985524"
---
# <span data-ttu-id="37b52-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="37b52-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="37b52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37b52-102">SYNOPSIS</span></span>
<span data-ttu-id="37b52-103">Tworzy/aktualizuje obiekt ACL elementu ACL elementu ACL (dataLake gen2), którego można używać w Update-AzDataLakeGen2Item cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37b52-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="37b52-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="37b52-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="37b52-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="37b52-105">DESCRIPTION</span></span>
<span data-ttu-id="37b52-106">Polecenie cmdlet **Set-AzDataLakeGen2ItemAclObject** tworzy/aktualizuje obiekt ACL elementu ACL elementu DataLake gen2, którego można użyć w Update-AzDataLakeGen2Item cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37b52-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="37b52-107">Jeśli nowy wpis ACL z tym samym elementem AccessControlType/EntityId/DefaultScope nie istnieje w wejściowym aclu, utworzy nowy wpis ACL, a w innym przypadku zaktualizuje uprawnienia istniejącego wpisu ACL.</span><span class="sxs-lookup"><span data-stu-id="37b52-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="37b52-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="37b52-108">EXAMPLES</span></span>

### <span data-ttu-id="37b52-109">Przykład 1. Tworzenie obiektu ACL z wpisem 3 ACL i aktualizowanie listy ACL w katalogu</span><span class="sxs-lookup"><span data-stu-id="37b52-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="37b52-110">To polecenie tworzy obiekt ACL z 3 pozycjami ACL (użyj parametru -InputObject, aby dodać wpis acl do istniejącego obiektu acl) i aktualizuje wartość ACL w katalogu.</span><span class="sxs-lookup"><span data-stu-id="37b52-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="37b52-111">Przykład 2. Tworzenie obiektu ACL z 4 pozycjami ACL i aktualizowanie uprawnień istniejącego wpisu ACL</span><span class="sxs-lookup"><span data-stu-id="37b52-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

<span data-ttu-id="37b52-112">To polecenie najpierw tworzy obiekt ACL z 4 pozycjami listy ACL, a następnie ponownie uruchamia polecenie cmdlet z innymi uprawnieniami, ale z tym samym obiektem AccessControlType/EntityId/DefaultScope istniejącego wpisu ACL.</span><span class="sxs-lookup"><span data-stu-id="37b52-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="37b52-113">Następnie uprawnienia wpisu listy ACL zostaną zaktualizowane, ale nie zostanie dodany żaden nowy wpis ACL.</span><span class="sxs-lookup"><span data-stu-id="37b52-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="37b52-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37b52-114">PARAMETERS</span></span>

### <span data-ttu-id="37b52-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="37b52-115">-AccessControlType</span></span>
<span data-ttu-id="37b52-116">Istnieją cztery typy: "użytkownik" udziela praw właścicielowi lub nazwanemu użytkownikowi, "grupa" udziela praw grupie posiadającej lub nazwanej grupie, "maska" ogranicza prawa przyznane nazwanych użytkownikom i członkom grup, a "inne" udziela praw wszystkim użytkownikom, których nie znaleziono w żadnych innych wpisach.</span><span class="sxs-lookup"><span data-stu-id="37b52-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b52-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="37b52-117">-DefaultScope</span></span>
<span data-ttu-id="37b52-118">Ustaw ten parametr, aby wskazać, że wpis ACE należy do domyślnej listy ACL dla katalogu; w przeciwnym razie zakres jest niejawny, a wpis ACE należy do listy kontroli dostępu.</span><span class="sxs-lookup"><span data-stu-id="37b52-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="37b52-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="37b52-119">-EntityId</span></span>
<span data-ttu-id="37b52-120">Identyfikator użytkownika lub grupy.</span><span class="sxs-lookup"><span data-stu-id="37b52-120">The user or group identifier.</span></span>
<span data-ttu-id="37b52-121">Jest ona pominięta w przypadku wpisów "mask" i "other" programu AccessControlType.</span><span class="sxs-lookup"><span data-stu-id="37b52-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="37b52-122">Identyfikator użytkownika lub grupy jest również pominięty dla właściciela i właściciela grupy.</span><span class="sxs-lookup"><span data-stu-id="37b52-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b52-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37b52-123">-InputObject</span></span>
<span data-ttu-id="37b52-124">W przypadku wprowadzania obiektu PSPathAccessControlEntry nowy element ACL zostanie dodać jako nowy element obiektu \[ \] wejściowego PSPathAccessControlEntry. \[ \]</span><span class="sxs-lookup"><span data-stu-id="37b52-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b52-125">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="37b52-125">-Permission</span></span>
<span data-ttu-id="37b52-126">Pole uprawnienia to 3-znakowa sekwencja, w której pierwszy znak to "r", aby udzielić dostępu do odczytu, drugi znak to "w" w celu udzielenia dostępu do zapisu, a trzeci znak to "x" w celu udzielenia uprawnienia wykonywania.</span><span class="sxs-lookup"><span data-stu-id="37b52-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="37b52-127">Jeśli nie udzielono dostępu, znak "-" jest używany do oznaczania, że uprawnienie zostanie odrzucone.</span><span class="sxs-lookup"><span data-stu-id="37b52-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b52-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b52-128">CommonParameters</span></span>
<span data-ttu-id="37b52-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37b52-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b52-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37b52-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b52-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37b52-131">INPUTS</span></span>

### <span data-ttu-id="37b52-132">Brak</span><span class="sxs-lookup"><span data-stu-id="37b52-132">None</span></span>

## <span data-ttu-id="37b52-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37b52-133">OUTPUTS</span></span>

### <span data-ttu-id="37b52-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="37b52-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="37b52-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="37b52-135">NOTES</span></span>

## <span data-ttu-id="37b52-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37b52-136">RELATED LINKS</span></span>
