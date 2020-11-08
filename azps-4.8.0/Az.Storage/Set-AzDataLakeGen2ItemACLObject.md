---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219734"
---
# <span data-ttu-id="041f4-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="041f4-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="041f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="041f4-102">SYNOPSIS</span></span>
<span data-ttu-id="041f4-103">Tworzy/aktualizuje obiekt Gen2 ACL elementu datalake, którego można użyć w Update-AzDataLakeGen2Item polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="041f4-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="041f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="041f4-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="041f4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="041f4-105">DESCRIPTION</span></span>
<span data-ttu-id="041f4-106">Polecenie cmdlet **Set-AzDataLakeGen2ItemAclObject** tworzy/AKTUALIZUJE obiekt ACL usługi datalake Gen2, który może być wykorzystywany w Update-AzDataLakeGen2Item polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="041f4-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="041f4-107">Jeśli nowy wpis ACL o tej samej AccessControlType/EntityId/DefaultScope nie istnieje na liście ACL danych wejściowych, zostanie utworzony nowy wpis ACL, w przeciwnym razie uprawnienia do istniejącego wpisu listy ACL.</span><span class="sxs-lookup"><span data-stu-id="041f4-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="041f4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="041f4-108">EXAMPLES</span></span>

### <span data-ttu-id="041f4-109">Przykład 1: Tworzenie obiektu ACL z 3 wpisami ACL i aktualizowanie listy ACL w katalogu</span><span class="sxs-lookup"><span data-stu-id="041f4-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
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

<span data-ttu-id="041f4-110">To polecenie tworzy obiekt ACL z trzema wpisami listy ACL (Use-Inputobject, aby dodać wpis ACL do istniejącego obiektu ACL), i aktualizuje listę ACL w katalogu.</span><span class="sxs-lookup"><span data-stu-id="041f4-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="041f4-111">Przykład 2: Tworzenie obiektu ACL z czterema wpisami list ACL i aktualizowanie uprawnień do istniejącego wpisu listy ACL</span><span class="sxs-lookup"><span data-stu-id="041f4-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
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

<span data-ttu-id="041f4-112">To polecenie najpierw tworzy obiekt ACL z czterema wpisami listy ACL, a następnie ponownie uruchamia polecenie cmdlet z innymi uprawnieniami, ale ten sam AccessControlType/EntityId/DefaultScope z istniejącego wpisu ACL.</span><span class="sxs-lookup"><span data-stu-id="041f4-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="041f4-113">Następnie uprawnienie do wpisu listy ACL zostanie zaktualizowane, ale nie zostanie dodany nowy wpis listy ACL.</span><span class="sxs-lookup"><span data-stu-id="041f4-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="041f4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="041f4-114">PARAMETERS</span></span>

### <span data-ttu-id="041f4-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="041f4-115">-AccessControlType</span></span>
<span data-ttu-id="041f4-116">Istnieją cztery typy: "użytkownik" udziela praw właścicielowi lub nazwanemu użytkownikowi, "Group" udziela praw członkowi grupy lub nazwanej grupie, "maska" ogranicza prawa przyznane pozostałym użytkownikom i członkom grup, a "inne" przyznaje prawa wszystkim użytkownikom, których nie ma w żadnym innym wpisie.</span><span class="sxs-lookup"><span data-stu-id="041f4-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

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

### <span data-ttu-id="041f4-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="041f4-117">-DefaultScope</span></span>
<span data-ttu-id="041f4-118">Ustaw ten parametr, aby wskazać, że wpis ACE należy do domyślnego ACL dla katalogu. w przeciwnym razie zakres jest niejawny, a wpis ACE należy do listy ACL programu Access.</span><span class="sxs-lookup"><span data-stu-id="041f4-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="041f4-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="041f4-119">-EntityId</span></span>
<span data-ttu-id="041f4-120">Identyfikator użytkownika lub grupy.</span><span class="sxs-lookup"><span data-stu-id="041f4-120">The user or group identifier.</span></span>
<span data-ttu-id="041f4-121">Jest ona pomijana dla wpisów AccessControlType "maska" i "inne".</span><span class="sxs-lookup"><span data-stu-id="041f4-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="041f4-122">Identyfikator użytkownika lub grupy jest również pomijany dla właściciela i grupy będącej właścicielem.</span><span class="sxs-lookup"><span data-stu-id="041f4-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="041f4-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="041f4-123">-InputObject</span></span>
<span data-ttu-id="041f4-124">Jeśli wprowadzasz obiekt PSPathAccessControlEntry, dodamy \[ \] nową listę ACL jako nowy element wejściowego \[ \] obiektu PSPathAccessControlEntry.</span><span class="sxs-lookup"><span data-stu-id="041f4-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

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

### <span data-ttu-id="041f4-125">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="041f4-125">-Permission</span></span>
<span data-ttu-id="041f4-126">Pole uprawnienia jest sekwencją 3-znakową, w której pierwszym znakiem jest "r", aby udzielić dostępu do odczytu, drugi znak jest literą "w", aby uzyskać dostęp do zapisu, a trzeci znak to "x", aby udzielić uprawnienia EXECUTE.</span><span class="sxs-lookup"><span data-stu-id="041f4-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="041f4-127">Jeśli nie zostanie udzielony dostęp, znak "-" jest oznaczany brakiem uprawnień.</span><span class="sxs-lookup"><span data-stu-id="041f4-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

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

### <span data-ttu-id="041f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="041f4-128">CommonParameters</span></span>
<span data-ttu-id="041f4-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="041f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="041f4-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="041f4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="041f4-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="041f4-131">INPUTS</span></span>

### <span data-ttu-id="041f4-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="041f4-132">None</span></span>

## <span data-ttu-id="041f4-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="041f4-133">OUTPUTS</span></span>

### <span data-ttu-id="041f4-134">Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="041f4-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="041f4-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="041f4-135">NOTES</span></span>

## <span data-ttu-id="041f4-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="041f4-136">RELATED LINKS</span></span>
